---
title: Auditoría de Seguridad — Clínica Odontológica
info: Proyecto Integrador de Auditoría de Sistemas
transition: slide-left
---

<!-- Diapositiva 1: Portada -->

<div class="portada">
  <div class="portada-titulo">
    <h1>Proyecto Integrador de Auditoría de Sistemas</h1>
    <p class="subtitulo">Auditoría de Seguridad de la Información</p>
    <p class="subtitulo-menor">El Tigre - Anzoátegui</p>
    <p class="estandar">ISO/IEC 27001:2022</p>
  </div>
  <div class="portada-datos">
    <p><strong>Juliano Cardona</strong></p>
    <p>C.I.: V-32.281.199</p>
    <p>Auditoría de Sistemas</p>
    <p>Marzo 2026</p>
  </div>
</div>

<style>
.portada {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 100%;
  text-align: center;
}
.portada-titulo h1 {
  color: #076678;
  font-size: 2.2em;
  margin-bottom: 0.3em;
  line-height: 1.2;
}
.subtitulo {
  color: #3c3836;
  font-size: 1.3em;
  margin: 0.2em 0;
}
.subtitulo-menor {
  color: #504945;
  font-size: 1.1em;
  margin: 0.2em 0;
}
.estandar {
  display: inline-block;
  background: #076678;
  color: #fbf1c7;
  padding: 0.3em 1.2em;
  border-radius: 6px;
  font-size: 1em;
  margin-top: 1em;
  font-weight: bold;
}
.portada-datos {
  margin-top: 2.5em;
  color: #665c54;
  font-size: 0.95em;
  line-height: 1.6;
}
</style>

---

<!-- Diapositiva 2: Entorno Auditado -->

<h1 class="slide-title">Entorno Auditado</h1>

<div class="dos-columnas">
  <div class="col-img">
    <img src="/05_diagrama_red.png" class="img-full" />
  </div>
  <div class="col-datos">
    <div class="ficha">
      <div class="ficha-item">
        <span class="ficha-label">Organización</span>
        <span>Clínica odontológica, 8 años operando</span>
      </div>
      <div class="ficha-item">
        <span class="ficha-label">Ubicación</span>
        <span>Zona este, Barquisimeto, Edo. Lara</span>
      </div>
      <div class="ficha-item">
        <span class="ficha-label">Infraestructura</span>
        <span>4 consultorios · 6 PCs · 1 servidor improvisado</span>
      </div>
      <div class="ficha-item">
        <span class="ficha-label">Pacientes</span>
        <span>~25 diarios · 9 empleados</span>
      </div>
      <div class="ficha-item ficha-critico">
        <span class="ficha-label ficha-label-rojo">Personal TI</span>
        <span>Ninguno. Técnico externo por demanda</span>
      </div>
      <div class="ficha-item ficha-critico">
        <span class="ficha-label ficha-label-rojo">Sistema clínico</span>
        <span>Proveedor cerró operaciones hace 1 año</span>
      </div>
    </div>
  </div>
</div>

<style>
.dos-columnas {
  display: grid;
  grid-template-columns: 1.3fr 1fr;
  gap: 1.5em;
  height: 85%;
  align-items: center;
}
.col-img {
  display: flex;
  align-items: center;
  justify-content: center;
}
.img-full {
  max-height: 420px;
  max-width: 100%;
  border-radius: 8px;
  border: 2px solid #d5c4a1;
}
.ficha {
  display: flex;
  flex-direction: column;
  gap: 0.6em;
}
.ficha-item {
  background: #ebdbb2;
  padding: 0.5em 0.8em;
  border-radius: 6px;
  font-size: 0.82em;
  line-height: 1.4;
  border-left: 4px solid #076678;
}
.ficha-critico {
  background: #f9e79f;
  border-left: 4px solid #cc241d;
}
.ficha-label {
  display: block;
  font-weight: bold;
  color: #076678;
  font-size: 0.85em;
  margin-bottom: 0.1em;
}
.ficha-label-rojo {
  color: #cc241d;
}
</style>

---

<!-- Diapositiva 3: Marco Normativo y Alcance -->

<h1 class="slide-title">Marco Normativo y Alcance</h1>

<div class="marco-grid">
  <div class="marco-estandar">
    <h3>📋 Estándar seleccionado</h3>
    <p class="estandar-nombre">ISO/IEC 27001:2022</p>
    <p class="estandar-razon">Datos clínicos sensibles → prioridad en confidencialidad</p>
    <p class="complementos"><strong>Complemento:</strong> NIST SP 800-66 · CIS Benchmarks</p>
  </div>

  <div class="marco-metodologia">
    <h3>🔄 Metodología PHVA</h3>
    <div class="phva">
      <span class="phva-p">Planificar</span>
      <span class="phva-flecha">→</span>
      <span class="phva-h">Hacer</span>
      <span class="phva-flecha">→</span>
      <span class="phva-v">Verificar</span>
      <span class="phva-flecha">→</span>
      <span class="phva-a">Actuar</span>
    </div>
  </div>

  <div class="marco-dominios">
    <h3>🎯 Dominios auditados</h3>
    <table class="tabla-dominios">
      <thead>
        <tr>
          <th>Dominio</th>
          <th>Controles ISO 27001</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td><strong>Seguridad Física</strong></td>
          <td>A.7.1, A.7.2, A.7.4, A.7.5, A.7.8</td>
        </tr>
        <tr>
          <td><strong>Respaldos y Continuidad</strong></td>
          <td>A.8.13, A.8.14</td>
        </tr>
        <tr>
          <td><strong>Acceso Lógico</strong></td>
          <td>A.5.15, A.5.17, A.5.18, A.8.5, A.8.15</td>
        </tr>
      </tbody>
    </table>
  </div>
</div>

<style>
.marco-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  grid-template-rows: auto auto;
  gap: 1em;
  height: 85%;
}
.marco-estandar {
  background: #ebdbb2;
  padding: 1em;
  border-radius: 8px;
  border-left: 5px solid #076678;
}
.marco-estandar h3 { margin: 0 0 0.4em 0; color: #076678; font-size: 1em; }
.estandar-nombre {
  font-size: 1.3em;
  font-weight: bold;
  color: #076678;
  margin: 0.2em 0;
}
.estandar-razon { color: #504945; font-size: 0.85em; margin: 0.3em 0; }
.complementos { font-size: 0.8em; color: #665c54; margin-top: 0.5em; }
.marco-metodologia {
  background: #ebdbb2;
  padding: 1em;
  border-radius: 8px;
  border-left: 5px solid #98971a;
  display: flex;
  flex-direction: column;
  justify-content: center;
}
.marco-metodologia h3 { margin: 0 0 0.6em 0; color: #98971a; font-size: 1em; }
.phva {
  display: flex;
  align-items: center;
  gap: 0.4em;
  flex-wrap: wrap;
  justify-content: center;
}
.phva-p, .phva-h, .phva-v, .phva-a {
  padding: 0.4em 0.8em;
  border-radius: 6px;
  font-weight: bold;
  color: #fbf1c7;
  font-size: 0.9em;
}
.phva-p { background: #076678; }
.phva-h { background: #98971a; }
.phva-v { background: #d79921; }
.phva-a { background: #cc241d; }
.phva-flecha { color: #928374; font-size: 1.2em; }
.marco-dominios {
  grid-column: 1 / -1;
  background: #ebdbb2;
  padding: 1em;
  border-radius: 8px;
}
.marco-dominios h3 { margin: 0 0 0.5em 0; color: #3c3836; font-size: 1em; }
.tabla-dominios {
  width: 100%;
  border-collapse: collapse;
  font-size: 0.85em;
}
.tabla-dominios th {
  background: #076678;
  color: #fbf1c7;
  padding: 0.5em 0.8em;
  text-align: left;
}
.tabla-dominios td {
  padding: 0.5em 0.8em;
  border-bottom: 1px solid #d5c4a1;
  color: #3c3836;
}
.tabla-dominios tr:nth-child(even) td { background: #f2e5bc; }
</style>

---

<!-- Diapositiva 4: Resultados de la Evaluación -->

<h1 class="slide-title">Resultados de la Evaluación</h1>

<div class="resultados-grid">
  <div class="resultado-img">
    <img src="/01_cumplimiento_general.png" class="img-chart" />
  </div>
  <div class="resultado-img">
    <img src="/02_cumplimiento_dominio.png" class="img-chart" />
  </div>
</div>

<div class="resultado-resumen">
  <div class="stat-box stat-rojo">
    <span class="stat-numero">14</span>
    <span class="stat-label">No cumplen</span>
  </div>
  <div class="stat-box stat-amarillo">
    <span class="stat-numero">4</span>
    <span class="stat-label">Parcial</span>
  </div>
  <div class="stat-box stat-verde">
    <span class="stat-numero">0</span>
    <span class="stat-label">Cumplen</span>
  </div>
  <div class="stat-box stat-gris">
    <span class="stat-numero">18</span>
    <span class="stat-label">Evaluados</span>
  </div>
</div>

<style>
.resultados-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 1em;
  height: 65%;
  align-items: center;
}
.img-chart {
  max-height: 340px;
  max-width: 100%;
  border-radius: 8px;
  border: 1px solid #d5c4a1;
}
.resultado-resumen {
  display: flex;
  gap: 1em;
  justify-content: center;
  margin-top: 0.5em;
}
.stat-box {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 0.5em 1.5em;
  border-radius: 8px;
  min-width: 100px;
}
.stat-numero { font-size: 1.8em; font-weight: bold; color: #fbf1c7; }
.stat-label { font-size: 0.8em; color: #fbf1c7; margin-top: 0.1em; }
.stat-rojo { background: #cc241d; }
.stat-amarillo { background: #d79921; }
.stat-amarillo .stat-numero, .stat-amarillo .stat-label { color: #3c3836; }
.stat-verde { background: #98971a; }
.stat-gris { background: #928374; }
</style>

---

<!-- Diapositiva 5: Hallazgos Críticos — Riesgo ALTO -->

<h1 class="slide-title titulo-rojo">Hallazgos Críticos — Riesgo ALTO</h1>

<div class="hallazgos-grid">
  <div class="hallazgo hallazgo-alto">
    <div class="hal-header">
      <span class="hal-badge hal-badge-alto">ALTO</span>
      <span class="hal-codigo">HAL-001</span>
    </div>
    <h3>Respaldos sin base de datos clínica</h3>
    <ul>
      <li>Solo 2 copias en 4 meses (cada 74 días)</li>
      <li><strong>NO incluyen volcado MySQL</strong></li>
      <li>8 años de historiales en 1 disco HDD</li>
      <li>Nunca se probó restaurar</li>
      <li>Pendrive sin cifrado en cajón de recepción</li>
    </ul>
  </div>

  <div class="hallazgo hallazgo-alto">
    <div class="hal-header">
      <span class="hal-badge hal-badge-alto">ALTO</span>
      <span class="hal-codigo">HAL-002</span>
    </div>
    <h3>Cuenta genérica compartida</h3>
    <ul>
      <li>1 cuenta «clinica» para 6 personas</li>
      <li>PIN de 4 dígitos (10.000 combinaciones)</li>
      <li>Sin roles ni permisos diferenciados</li>
      <li>Módulo de logs deshabilitado</li>
      <li>Imposible rastrear quién hizo qué</li>
    </ul>
  </div>

  <div class="hallazgo hallazgo-alto ancho-completo">
    <div class="hal-header">
      <span class="hal-badge hal-badge-alto">ALTO</span>
      <span class="hal-codigo">HAL-003</span>
    </div>
    <h3>Servidor sin protección física</h3>
    <div class="hal-horizontal">
      <ul>
        <li>Mueble abierto en oficina sin cerradura</li>
        <li>Polvo acumulado en componentes</li>
      </ul>
      <ul>
        <li>UPS de 4 años, baterías nunca reemplazadas</li>
        <li>Sin detección de incendios ni extintor CO₂</li>
      </ul>
      <ul>
        <li>Aire acondicionado apagado fuera de horario</li>
        <li>27 °C con aire encendido</li>
      </ul>
    </div>
  </div>
</div>

<style>
.titulo-rojo { color: #cc241d !important; }
.hallazgos-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 0.8em;
  height: 85%;
}
.ancho-completo { grid-column: 1 / -1; }
.hal-horizontal {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  gap: 0.5em;
}
.hal-horizontal ul { font-size: 0.95em; }
.hallazgo {
  background: #ebdbb2;
  padding: 0.7em 0.9em;
  border-radius: 8px;
  border-left: 5px solid #928374;
  font-size: 0.78em;
}
.hallazgo h3 {
  margin: 0.3em 0;
  color: #3c3836;
  font-size: 1.05em;
}
.hallazgo ul {
  margin: 0.3em 0;
  padding-left: 1.2em;
  line-height: 1.5;
  color: #504945;
}
.hal-header {
  display: flex;
  align-items: center;
  gap: 0.5em;
}
.hal-badge {
  padding: 0.15em 0.6em;
  border-radius: 4px;
  font-size: 0.75em;
  font-weight: bold;
  color: #fbf1c7;
}
.hal-codigo {
  font-weight: bold;
  color: #665c54;
  font-size: 0.9em;
}
.hallazgo-alto { border-left-color: #cc241d; }
.hal-badge-alto { background: #cc241d; }
</style>

---

<!-- Diapositiva 6: Hallazgos Medio / Bajo + Matriz de Riesgo -->

<h1 class="slide-title">Hallazgos Medio / Bajo + Matriz de Riesgo</h1>

<div class="mb-grid">
  <div class="mb-col">
    <div class="mb-hallazgo mb-medio">
      <div class="mb-header">
        <span class="mb-badge mb-badge-medio">MEDIO</span>
        <span class="mb-codigo">HAL-004</span>
      </div>
      <h3 class="mb-titulo">WiFi compartido con pacientes</h3>
      <ul class="mb-lista">
        <li>SSID único sin segmentación de red</li>
        <li>Pacientes en mismo segmento que el servidor</li>
        <li>Router con credenciales por defecto</li>
      </ul>
    </div>
    <div class="mb-hallazgo mb-medio">
      <div class="mb-header">
        <span class="mb-badge mb-badge-medio">MEDIO</span>
        <span class="mb-codigo">HAL-005</span>
      </div>
      <h3 class="mb-titulo">Windows Home sin gestión centralizada</h3>
      <ul class="mb-lista">
        <li>Sin Active Directory posible</li>
        <li>Sin bloqueo de pantalla ni políticas</li>
      </ul>
    </div>
    <div class="mb-hallazgo mb-bajo">
      <div class="mb-header">
        <span class="mb-badge mb-badge-bajo">BAJO</span>
        <span class="mb-codigo">HAL-006</span>
      </div>
      <h3 class="mb-titulo">Sin contrato de soporte técnico</h3>
      <ul class="mb-lista">
        <li>Todo depende de 1 técnico informal</li>
        <li>Cero documentación de infraestructura</li>
      </ul>
    </div>
  </div>
  <div class="mb-col-img">
    <img src="/04_matriz_riesgo.png" class="mb-imagen" />
  </div>
</div>

<style>
.mb-grid {
  display: grid;
  grid-template-columns: 1fr 1.2fr;
  gap: 1em;
  height: 88%;
  align-items: center;
}
.mb-col {
  display: flex;
  flex-direction: column;
  gap: 0.6em;
}
.mb-col-img {
  display: flex;
  align-items: center;
  justify-content: center;
}
.mb-imagen {
  max-width: 100%;
  max-height: 420px;
  border-radius: 8px;
  border: 1px solid #d5c4a1;
}
.mb-hallazgo {
  background: #ebdbb2;
  padding: 0.7em 0.9em;
  border-radius: 8px;
  border-left: 5px solid #928374;
  font-size: 0.78em;
}
.mb-medio {
  border-left-color: #d79921;
}
.mb-bajo {
  border-left-color: #b57614;
}
.mb-header {
  display: flex;
  align-items: center;
  gap: 0.5em;
}
.mb-badge {
  padding: 0.15em 0.6em;
  border-radius: 4px;
  font-size: 0.75em;
  font-weight: bold;
  color: #fbf1c7;
}
.mb-badge-medio {
  background: #d79921;
  color: #3c3836;
}
.mb-badge-bajo {
  background: #b57614;
}
.mb-codigo {
  font-weight: bold;
  color: #665c54;
  font-size: 0.9em;
}
.mb-titulo {
  margin: 0.3em 0;
  color: #3c3836;
  font-size: 1.05em;
}
.mb-lista {
  margin: 0.3em 0;
  padding-left: 1.2em;
  line-height: 1.5;
  color: #504945;
}
</style>

---

<!-- Diapositiva 7: Evidencias de la Inspección -->

<h1 class="slide-title">Evidencias de la Inspección</h1>

<div class="ev-grid">
  <div class="ev-card">
    <img src="/foto-servidor.jpg" class="ev-foto" />
    <p class="ev-caption"><strong>Servidor en mueble abierto</strong><br/>Oficina administrativa, sin cerradura</p>
  </div>
  <div class="ev-card">
    <img src="/foto-cables.jpg" class="ev-foto" />
    <p class="ev-caption"><strong>Cables expuestos</strong><br/>Tramo oficina-pasillo sin canaleta</p>
  </div>
  <div class="ev-card">
    <img src="/foto-ups.jpg" class="ev-foto" />
    <p class="ev-caption"><strong>UPS genérica</strong><br/>4 años, baterías nunca reemplazadas</p>
  </div>
  <div class="ev-card">
    <img src="/foto-pendrive.jpg" class="ev-foto" />
    <p class="ev-caption"><strong>Pendrive de respaldos</strong><br/>Sin cifrado, cajón de recepción</p>
  </div>
  <div class="ev-card">
    <img src="/foto-login.jpg" class="ev-foto" />
    <p class="ev-caption"><strong>Login del sistema</strong><br/>Cuenta compartida, PIN 4 dígitos</p>
  </div>
  <div class="ev-card">
    <img src="/foto-pendrive-contenido.jpg" class="ev-foto" />
    <p class="ev-caption"><strong>Contenido del pendrive</strong><br/>Sin volcado .sql de MySQL</p>
  </div>
</div>

<p class="ev-fecha">Inspección física: 10 de julio de 2025 — Revisión lógica: 11 de julio de 2025</p>

<style>
.ev-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 0.7em;
  margin-top: 0.3em;
}
.ev-card {
  background: #ebdbb2;
  border-radius: 8px;
  overflow: hidden;
  border: 1px solid #d5c4a1;
}
.ev-foto {
  width: 100%;
  height: 125px;
  object-fit: cover;
  display: block;
}
.ev-caption {
  padding: 0.4em 0.5em;
  font-size: 0.7em;
  color: #504945;
  line-height: 1.35;
  margin: 0;
}
.ev-fecha {
  text-align: center;
  font-size: 0.72em;
  color: #928374;
  margin-top: 0.4em;
}
</style>

---

<!-- Diapositiva 8: Recomendaciones Priorizadas -->

<h1 class="slide-title titulo-verde">Recomendaciones Priorizadas</h1>

<div class="recomendaciones-grid">
  <div class="rec-grupo rec-rojo">
    <h3>🔴 Inmediatas — 0 a 30 días</h3>
    <div class="rec-item"><span class="rec-tag">HAL-001</span> Implementar mysqldump diario automatizado <span class="rec-costo">$0</span></div>
    <div class="rec-item"><span class="rec-tag">HAL-001</span> 2 discos externos con rotación + cifrado BitLocker</div>
    <div class="rec-item"><span class="rec-tag">HAL-001</span> Ejecutar prueba de restauración y documentar</div>
    <div class="rec-item"><span class="rec-tag">HAL-002</span> Crear cuentas individuales con roles diferenciados</div>
    <div class="rec-item"><span class="rec-tag">HAL-002</span> Habilitar logs del sistema clínico</div>
    <div class="rec-item"><span class="rec-tag">HAL-004</span> Cambiar credenciales del router <span class="rec-costo">24h</span></div>
  </div>

  <div class="rec-grupo rec-amarillo">
    <h3>🟠 Corto plazo — 31 a 90 días</h3>
    <div class="rec-item"><span class="rec-tag">HAL-003</span> Rack cerrado con llave o mueble con acceso restringido</div>
    <div class="rec-item"><span class="rec-tag">HAL-003</span> Detector de humo + extintor CO₂</div>
    <div class="rec-item"><span class="rec-tag">HAL-003</span> Reemplazar baterías UPS o adquirir nueva ≥1.5 kVA</div>
    <div class="rec-item"><span class="rec-tag">HAL-004</span> Segmentar red WiFi (SSID separado para pacientes)</div>
    <div class="rec-item"><span class="rec-tag">HAL-005</span> Configurar bloqueo de pantalla en todos los PCs</div>
  </div>

  <div class="rec-grupo rec-verde">
    <h3>🟡 Mediano plazo — 60 a 180 días</h3>
    <div class="rec-item"><span class="rec-tag">HAL-006</span> Formalizar contrato de soporte con SLA</div>
    <div class="rec-item"><span class="rec-tag">HAL-006</span> Documentar infraestructura y credenciales</div>
    <div class="rec-item"><span class="rec-tag">HAL-006</span> Evaluar migración a sistema clínico con soporte activo</div>
  </div>
</div>

<p class="rec-nota">💡 La mayoría de acciones críticas son de <strong>bajo costo o costo cero</strong></p>

<style>
.titulo-verde { color: #98971a !important; }
.recomendaciones-grid {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  gap: 0.7em;
  height: 78%;
}
.rec-grupo {
  background: #ebdbb2;
  padding: 0.7em;
  border-radius: 8px;
  font-size: 0.72em;
}
.rec-rojo { border-top: 4px solid #cc241d; }
.rec-amarillo { border-top: 4px solid #d79921; }
.rec-verde { border-top: 4px solid #98971a; }
.rec-grupo h3 { margin: 0 0 0.5em 0; font-size: 1.05em; color: #3c3836; }
.rec-item {
  background: #fbf1c7;
  padding: 0.35em 0.5em;
  border-radius: 4px;
  margin-bottom: 0.35em;
  line-height: 1.4;
  color: #504945;
}
.rec-tag {
  background: #076678;
  color: #fbf1c7;
  padding: 0.1em 0.4em;
  border-radius: 3px;
  font-size: 0.8em;
  font-weight: bold;
  margin-right: 0.3em;
}
.rec-costo {
  background: #98971a;
  color: #fbf1c7;
  padding: 0.1em 0.4em;
  border-radius: 3px;
  font-size: 0.8em;
  font-weight: bold;
  float: right;
}
.rec-nota {
  text-align: center;
  font-size: 0.85em;
  color: #504945;
  margin-top: 0.3em;
}
</style>

---

<!-- Diapositiva 9: Cronograma de Implementación -->

<h1 class="slide-title">Cronograma de Implementación</h1>

<div class="gantt-container">
  <img src="/06_plan_remediacion.png" class="img-gantt" />
</div>

<div class="gantt-hitos">
  <div class="hito">
    <span class="hito-dia">Día 7</span>
    <span class="hito-desc">Respaldo mysqldump funcional</span>
  </div>
  <div class="hito">
    <span class="hito-dia">Día 30</span>
    <span class="hito-desc">Cuentas individuales + logs activos</span>
  </div>
  <div class="hito">
    <span class="hito-dia">Día 60</span>
    <span class="hito-desc">Servidor protegido físicamente</span>
  </div>
  <div class="hito">
    <span class="hito-dia">Día 90</span>
    <span class="hito-desc">Contrato de soporte formalizado</span>
  </div>
  <div class="hito hito-seguimiento">
    <span class="hito-dia">Día 120</span>
    <span class="hito-desc">Auditoría de seguimiento</span>
  </div>
</div>

<style>
.gantt-container {
  display: flex;
  justify-content: center;
  margin: 0.5em 0;
}
.img-gantt {
  max-width: 95%;
  max-height: 330px;
  border-radius: 8px;
  border: 1px solid #d5c4a1;
}
.gantt-hitos {
  display: flex;
  gap: 0.6em;
  justify-content: center;
  margin-top: 0.8em;
}
.hito {
  background: #ebdbb2;
  padding: 0.4em 0.7em;
  border-radius: 6px;
  font-size: 0.75em;
  text-align: center;
  border-top: 3px solid #076678;
}
.hito-seguimiento { border-top-color: #458588; background: #d5c4a1; }
.hito-dia {
  display: block;
  font-weight: bold;
  color: #076678;
  font-size: 1.05em;
}
.hito-desc {
  display: block;
  color: #504945;
  margin-top: 0.2em;
  line-height: 1.3;
}
</style>

---

<!-- Diapositiva 10: Conclusiones -->

<h1 class="slide-title">Conclusiones</h1>

<div class="cl-layout">
  <div class="cl-col">
    <div class="cl-item cl-neutral">
      <span class="cl-icono">⚠️</span>
      <div class="cl-texto">
        <strong>Nivel de madurez inexistente</strong>
        <span> en gestión de seguridad de la información. Sin políticas, sin personal de TI, sin contratos, sin documentación.</span>
      </div>
    </div>
    <div class="cl-item cl-critico">
      <span class="cl-icono">🔴</span>
      <div class="cl-texto">
        <strong>Riesgo más grave:</strong>
        <span> los historiales clínicos de 8 años residen en un único disco duro sin respaldo real. Una falla implica pérdida total e irreversible.</span>
      </div>
    </div>
    <div class="cl-item cl-neutral">
      <span class="cl-icono">🔐</span>
      <div class="cl-texto">
        <strong>Sin trazabilidad:</strong>
        <span> la cuenta genérica y los logs deshabilitados hacen imposible auditar quién accede o modifica datos clínicos sensibles.</span>
      </div>
    </div>
    <div class="cl-item cl-positivo">
      <span class="cl-icono">✅</span>
      <div class="cl-texto">
        <strong>Soluciones accesibles:</strong>
        <span> la mayoría de recomendaciones son de bajo costo. Un mysqldump automatizado cuesta $0 y protege 8 años de información.</span>
      </div>
    </div>
    <div class="cl-item cl-seguimiento">
      <span class="cl-icono">📅</span>
      <div class="cl-texto">
        <strong>Seguimiento:</strong>
        <span> auditoría de verificación propuesta a los 120 días para evaluar avances en la implementación.</span>
      </div>
    </div>
  </div>
  <div class="cl-col-img">
    <img src="/03_hallazgos_riesgo.png" class="cl-imagen" />
  </div>
</div>


<style>
.cl-layout {
  display: grid;
  grid-template-columns: 1.3fr 1fr;
  gap: 1em;
  height: 72%;
  align-items: center;
}
.cl-col {
  display: flex;
  flex-direction: column;
  gap: 0.5em;
}
.cl-col-img {
  display: flex;
  align-items: center;
  justify-content: center;
}
.cl-imagen {
  max-width: 100%;
  max-height: 300px;
  border-radius: 8px;
  border: 1px solid #d5c4a1;
}
.cl-item {
  display: flex;
  gap: 0.5em;
  background: #ebdbb2;
  padding: 0.5em 0.7em;
  border-radius: 6px;
  font-size: 0.78em;
  line-height: 1.4;
  color: #504945;
  border-left: 4px solid #928374;
}
.cl-neutral {
  border-left-color: #928374;
}
.cl-critico {
  border-left-color: #cc241d;
  background: #f9e79f;
}
.cl-positivo {
  border-left-color: #98971a;
}
.cl-seguimiento {
  border-left-color: #458588;
}
.cl-icono {
  font-size: 1.2em;
  flex-shrink: 0;
}
.cl-texto {
  display: flex;
  flex-direction: column;
  gap: 0.1em;
}
.cl-frase {
  text-align: center;
  font-style: italic;
  color: #076678;
  font-size: 0.9em;
  margin-top: 0.5em;
  padding: 0.5em;
  background: #ebdbb2;
  border-radius: 6px;
}
</style>
