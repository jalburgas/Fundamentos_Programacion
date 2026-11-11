
<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Clase Diseño de Software</title>
<script src="https://cdn.jsdelivr.net/npm/mermaid@10/dist/mermaid.min.js"></script>
<style>
  body {
    font-family: Arial, sans-serif;
    background: linear-gradient(135deg, #667eea, #764ba2);
    background-attachment: fixed;
    margin: 0;
    padding: 20px;
    color: #333;
    line-height: 1.6;
  }
  .container {
    max-width: 1000px;
    margin: 0 auto;
  }
  .hero {
    background: linear-gradient(135deg, #1e3c72, #6a3093);
    color: white;
    padding: 40px 20px;
    border-radius: 16px;
    text-align: center;
    box-shadow: 0 15px 40px rgba(0,0,0,0.4);
    margin-bottom: 25px;
  }
  .hero h1 { margin: 0 0 10px 0; font-size: 2.2em; }
  .hero h2 { margin: 0 0 20px 0; font-size: 1.1em; color: #ffd700; font-weight: normal; }

  .card {
    background: white;
    padding: 25px;
    border-radius: 14px;
    margin: 20px 0;
    box-shadow: 0 8px 25px rgba(0,0,0,0.15);
  }

  .title-bar {
    padding: 18px 25px;
    border-radius: 12px;
    color: white;
    font-size: 1.3em;
    font-weight: bold;
    margin: 30px 0 15px 0;
    box-shadow: 0 8px 20px rgba(0,0,0,0.3);
  }
  .t1 { background: linear-gradient(135deg, #2193b0, #6dd5ed); }
  .t2 { background: linear-gradient(135deg, #11998e, #38ef7d); }
  .t3 { background: linear-gradient(135deg, #8e2de2, #4a00e0); }
  .t4 { background: linear-gradient(135deg, #ee0979, #ff6a00); }
  .t5 { background: linear-gradient(135deg, #396afc, #2948ff); }

  .info-blue {
    background: #e3f2fd;
    border-left: 6px solid #2196f3;
    padding: 18px;
    border-radius: 10px;
    margin: 15px 0;
  }
  .info-green {
    background: #e8f5e9;
    border-left: 6px solid #4caf50;
    padding: 18px;
    border-radius: 10px;
    margin: 15px 0;
  }
  .info-purple {
    background: #f3e5f5;
    border-left: 6px solid #9c27b0;
    padding: 18px;
    border-radius: 10px;
    margin: 15px 0;
  }
  .info-pink {
    background: #fce4ec;
    border-left: 6px solid #e91e63;
    padding: 18px;
    border-radius: 10px;
    margin: 15px 0;
  }
  .warn {
    background: #fff3cd;
    border-left: 5px solid #ffc107;
    padding: 12px;
    border-radius: 8px;
    margin: 10px 0;
  }

  .exercise {
    background: linear-gradient(135deg, #f7971e, #ffd200);
    padding: 20px;
    border-radius: 12px;
    margin: 20px 0;
    color: #4a2600;
    box-shadow: 0 8px 20px rgba(247,151,30,0.4);
  }
  .exercise h3 { margin-top: 0; }

  .project {
    background: linear-gradient(135deg, #f093fb, #f5576c);
    padding: 30px;
    border-radius: 16px;
    margin: 30px 0;
    color: white;
    box-shadow: 0 15px 40px rgba(240,147,251,0.5);
  }
  .project h2 { margin-top: 0; }

  .summary {
    background: linear-gradient(135deg, #43cea2, #185a9d);
    padding: 25px;
    border-radius: 14px;
    margin: 30px 0;
    color: white;
    box-shadow: 0 10px 30px rgba(24,90,157,0.4);
  }
  .summary table { color: white; width: 100%; }
  .summary th { background: rgba(255,255,255,0.2); }
  .summary th, .summary td {
    padding: 10px;
    text-align: left;
    border-bottom: 1px solid rgba(255,255,255,0.2);
  }

  .tip {
    background: linear-gradient(135deg, #d4edda, #a5d6a7);
    border-left: 6px solid #28a745;
    padding: 18px;
    border-radius: 12px;
    margin: 25px 0;
    color: #1b5e20;
  }

  .footer {
    background: linear-gradient(135deg, #232526, #414345);
    padding: 30px;
    border-radius: 16px;
    text-align: center;
    color: white;
    margin-top: 30px;
    box-shadow: 0 10px 30px rgba(0,0,0,0.5);
  }
  .footer h3 { color: #ffd700; margin-top: 0; }

  table {
    width: 100%;
    border-collapse: collapse;
    margin: 15px 0;
  }
  th {
    background: #667eea;
    color: white;
    padding: 10px;
    text-align: left;
  }
  td {
    padding: 10px;
    border-bottom: 1px solid #ddd;
  }
  tr:nth-child(even) td { background: #f9f9fc; }

  .mermaid {
    background: #fafafa;
    padding: 15px;
    border-radius: 10px;
    margin: 15px 0;
    text-align: center;
  }

  ul, ol { margin: 10px 0 10px 25px; }

  @media (max-width: 600px) {
    .hero h1 { font-size: 1.5em; }
    .hero h2 { font-size: 0.9em; }
    .title-bar { font-size: 1.1em; padding: 14px 18px; }
  }
</style>
</head>
<body>
<div class="container">

  <div class="hero">
    <h1>🎓 Clase para Principiantes</h1>
    <h2>Diagramas de Flujo · UML · Sistemas · Procesos · Desarrollo</h2>
    <img src="https://img.shields.io/badge/Nivel-Principiante-brightgreen?style=for-the-badge" alt="Nivel">
    <img src="https://img.shields.io/badge/Duración-4%20horas-blue?style=for-the-badge" alt="Duración">
  </div>

  <div class="card">
    <h2>🎯 Objetivo de la Clase</h2>
    <p>Al finalizar serás capaz de:</p>
    <ul>
      <li>✅ Comprender los <b>diagramas de flujo</b></li>
      <li>✅ Entender <b>UML</b> y sus diagramas</li>
      <li>✅ Diseñar <b>sistemas</b> básicos</li>
      <li>✅ Modelar <b>procesos</b> de negocio</li>
      <li>✅ Conocer el <b>ciclo de vida del software</b></li>
    </ul>
    <p><b>⏱️ Duración:</b> 4 horas (2 sesiones de 2 horas)</p>
  </div>

  <div class="title-bar t1">📖 Módulo 1 · Diagramas de Flujo</div>

  <div class="info-blue">
    <h3>💡 ¿Qué es un diagrama de flujo?</h3>
    <p>Es una <b>representación gráfica de un algoritmo o proceso</b>, usando símbolos conectados por flechas que muestran la secuencia de pasos.</p>
  </div>

  <div class="card">
    <h3>🔣 Símbolos básicos</h3>
    <table>
      <tr><th>Símbolo</th><th>Nombre</th><th>Uso</th></tr>
      <tr><td>⬭</td><td><b>Inicio / Fin</b></td><td>Comienzo y final del proceso</td></tr>
      <tr><td>▭</td><td><b>Proceso</b></td><td>Acción o tarea</td></tr>
      <tr><td>◇</td><td><b>Decisión</b></td><td>Pregunta con caminos (Sí/No)</td></tr>
      <tr><td>▱</td><td><b>Entrada / Salida</b></td><td>Leer datos o mostrar resultados</td></tr>
      <tr><td>➡️</td><td><b>Flujo</b></td><td>Dirección del proceso</td></tr>
    </table>

    <h3>🧩 Ejemplo: Validar usuario</h3>
    <div class="mermaid">
flowchart TD
    A([Inicio]) --> B[/Leer usuario y contraseña/]
    B --> C{¿Datos correctos?}
    C -->|Sí| D[Mostrar bienvenida]
    C -->|No| E[Mostrar error]
    D --> F([Fin])
    E --> F
    </div>
  </div>

  <div class="exercise">
    <h3>✏️ Ejercicio 1</h3>
    <p>Dibuja el diagrama de flujo de: <b>"Sacar dinero de un cajero automático"</b>. Considera: insertar tarjeta, validar PIN, verificar saldo, entregar dinero.</p>
  </div>

  <div class="title-bar t2">📖 Módulo 2 · Introducción a UML</div>

  <div class="info-green">
    <h3>💡 ¿Qué es UML?</h3>
    <p><b>Unified Modeling Language</b> es un lenguaje visual estándar para <b>especificar, visualizar y documentar</b> sistemas de software.</p>
    <div class="warn">⚠️ UML <b>NO</b> es un lenguaje de programación, es un conjunto de <b>diagramas</b> para comunicar ideas.</div>
  </div>

  <div class="card">
    <h3>📊 Diagramas UML más usados</h3>

    <h4>1️⃣ Casos de Uso</h4>
    <div class="mermaid">
flowchart LR
    E[🧑 Estudiante] --> U1((Solicitar libro))
    E --> U2((Devolver libro))
    B[🧑 Bibliotecario] --> U3((Registrar libro))
    </div>

    <h4>2️⃣ Diagrama de Clases</h4>
    <div class="mermaid">
classDiagram
    class Libro {
        -titulo
        -autor
        +prestar()
        +devolver()
    }
    class Usuario {
        -nombre
        -id
        +solicitar()
    }
    Usuario "1" --> "*" Libro : solicita
    </div>

    <h4>3️⃣ Diagrama de Secuencia</h4>
    <div class="mermaid">
sequenceDiagram
    participant U as Usuario
    participant S as Sistema
    participant D as BaseDatos
    U->>S: login()
    S->>D: verificar()
    D-->>S: ok
    S-->>U: acceso concedido
    </div>
  </div>

  <div class="exercise">
    <h3>✏️ Ejercicio 2</h3>
    <p>Para una <b>app de comida a domicilio</b>, identifica: 3 actores, 5 casos de uso y dibuja el diagrama.</p>
  </div>

  <div class="title-bar t3">📖 Módulo 3 · Diseño de Sistemas</div>

  <div class="info-purple">
    <h3>💡 ¿Qué es el diseño de sistemas?</h3>
    <p>Es el proceso de <b>definir la arquitectura, componentes, módulos, interfaces y datos</b> de un sistema para satisfacer los requisitos.</p>
  </div>

  <div class="card">
    <h3>🔄 Fases del diseño</h3>
    <div class="mermaid">
flowchart LR
    A[1. Requisitos] --> B[2. Diseño arquitectónico]
    B --> C[3. Diseño detallado]
    C --> D[4. Implementación]
    </div>

    <h3>🧱 Componentes clave</h3>
    <table>
      <tr><th>Componente</th><th>Pregunta clave</th></tr>
      <tr><td>🏗️ <b>Arquitectura</b></td><td>¿Cliente-servidor? ¿Microservicios?</td></tr>
      <tr><td>📦 <b>Módulos</b></td><td>¿Cómo divido el sistema?</td></tr>
      <tr><td>🗄️ <b>Base de datos</b></td><td>¿Qué datos guardo?</td></tr>
      <tr><td>🖥️ <b>Interfaces</b></td><td>¿Cómo interactúa el usuario?</td></tr>
      <tr><td>🔒 <b>Seguridad</b></td><td>¿Cómo protejo los datos?</td></tr>
    </table>
  </div>

  <div class="exercise">
    <h3>✏️ Ejercicio 3</h3>
    <p>Diseña la arquitectura de una <b>app de tareas (to-do list)</b>: módulos, datos y comunicación.</p>
  </div>

  <div class="title-bar t4">📖 Módulo 4 · Diseño de Procesos</div>

  <div class="info-pink">
    <h3>💡 ¿Qué es un proceso?</h3>
    <p>Un <b>conjunto de actividades interrelacionadas</b> que transforman entradas en salidas con valor para el cliente.</p>
  </div>

  <div class="card">
    <h3>📐 Notación BPMN</h3>
    <table>
      <tr><th>Símbolo</th><th>Significado</th></tr>
      <tr><td>⚪</td><td>Evento de inicio / fin</td></tr>
      <tr><td>▭</td><td>Actividad / Tarea</td></tr>
      <tr><td>◇</td><td>Decisión (gateway)</td></tr>
      <tr><td>🏊</td><td>Swimlane (quién hace qué)</td></tr>
      <tr><td>➡️</td><td>Flujo del proceso</td></tr>
    </table>

    <h3>🏖️ Ejemplo: Aprobación de vacaciones</h3>
    <div class="mermaid">
flowchart TD
    A([Inicio]) --> B[Empleado solicita]
    B --> C[Jefe revisa]
    C --> D{¿Aprueba?}
    D -->|Sí| E[RRHH registra]
    D -->|No| F[Notificar rechazo]
    E --> G([Fin])
    F --> G
    </div>
  </div>

  <div class="exercise">
    <h3>✏️ Ejercicio 4</h3>
    <p>Modela el proceso de <b>"Compra en línea"</b>: inicio (elegir producto), fin (recibir producto), incluyendo pago, validación y envío.</p>
  </div>

  <div class="title-bar t5">📖 Módulo 5 · Desarrollo de Software</div>

  <div class="card">
    <h3>🔄 Ciclo de Vida (SDLC)</h3>
    <div class="mermaid">
flowchart LR
    A[1. Requisitos] --> B[2. Diseño]
    B --> C[3. Implementación]
    C --> D[4. Pruebas]
    D --> E[5. Despliegue]
    E --> F[6. Mantenimiento]
    F -.-> A
    </div>

    <h3>🧭 Metodologías</h3>
    <table>
      <tr><th>Metodología</th><th>Ventaja</th><th>Desventaja</th></tr>
      <tr><td><b>Cascada</b></td><td>Fácil de entender</td><td>Poco flexible</td></tr>
      <tr><td><b>Ágil (Scrum)</b></td><td>Se adapta al cambio</td><td>Requiere disciplina</td></tr>
    </table>

    <h3>👥 Roles típicos</h3>
    <table>
      <tr><th>Rol</th><th>Responsabilidad</th></tr>
      <tr><td>🎯 Product Owner</td><td>Define qué construir</td></tr>
      <tr><td>🏃 Scrum Master</td><td>Facilita el proceso ágil</td></tr>
      <tr><td>💻 Desarrollador</td><td>Construye el software</td></tr>
      <tr><td>🔍 QA / Tester</td><td>Verifica la calidad</td></tr>
    </table>

    <h3>🛠️ Herramientas</h3>
    <table>
      <tr><th>Propósito</th><th>Herramienta</th></tr>
      <tr><td>Diagramas de flujo</td><td><a href="https://app.diagrams.net">draw.io</a></td></tr>
      <tr><td>UML</td><td>draw.io · StarUML · PlantUML</td></tr>
      <tr><td>BPMN</td><td>Bizagi Modeler · Camunda</td></tr>
      <tr><td>Proyectos</td><td>Trello · Notion · GitHub Projects</td></tr>
    </table>
  </div>

  <div class="exercise">
    <h3>✏️ Ejercicio 5</h3>
    <p>En grupos de 3, elijan una app sencilla y definan: problema, funcionalidades, arquitectura y proceso principal.</p>
  </div>

  <div class="project">
    <h2>🏆 Proyecto Integrador</h2>
    <h3>📝 Sistema de Reservas de Canchas Deportivas</h3>
    <p>Crea un documento de 5-8 páginas con:</p>
    <ol>
      <li>✅ Diagrama de flujo del proceso de reserva</li>
      <li>✅ Diagrama de casos de uso (Jugador, Administrador)</li>
      <li>✅ Diagrama de clases (Cancha, Reserva, Usuario)</li>
      <li>✅ Diagrama de arquitectura (módulos)</li>
      <li>✅ Diagrama BPMN del proceso de pago</li>
      <li>✅ Descripción del ciclo de vida elegido</li>
    </ol>
  </div>

  <div class="summary">
    <h2>🎓 Resumen Final</h2>
    <table>
      <tr><th>Concepto</th><th>¿Qué aprendimos?</th></tr>
      <tr><td>📊 Diagramas de flujo</td><td>Representar pasos de un algoritmo</td></tr>
      <tr><td>🧩 UML</td><td>Modelar sistemas con casos de uso, clases y secuencia</td></tr>
      <tr><td>🏗️ Diseño de sistemas</td><td>Definir arquitectura, módulos y datos</td></tr>
      <tr><td>🔄 Diseño de procesos</td><td>Modelar flujos de negocio con BPMN</td></tr>
      <tr><td>⚙️ Desarrollo de software</td><td>Ciclo de vida y metodologías</td></tr>
    </table>
  </div>

  <div class="tip">
    <h3>💡 Consejo final</h3>
    <p>La mejor forma de aprender es <b>practicar</b>. Empieza con diagramas simples de cosas cotidianas y ve aumentando la complejidad.</p>
  </div>

  <div class="footer">
    <h3>⭐ ¡Si te sirvió, dale una estrella al repo! ⭐</h3>
    <p>Hecho con ❤️ para aprender diseño de software</p>
  </div>

</div>

<script>
  mermaid.initialize({ startOnLoad: true, theme: 'default' });
</script>
</body>
</html>


