
(label_aplicaciones)=
Aplicaciones de la minería de textos
====================================

Este tercer bloque analiza diversas aplicaciones de las técnicas de procesamiento del lenguaje natural. El profesor encargado de este bloque es [Yoan Gutiérrez][yoan url]. Colaboradores: [José I. Abbreu Salas][abreu url], [Javier Fernández Martínez][javi url], [Eduardo Grande Ruiz](https://cvnet.cpd.ua.es/curriculum-breve/es/grande-ruiz-eduardo/327690) y  [Juan Pablo Consuegra](https://cvnet.cpd.ua.es/curriculum-breve/es/consuegra-ayala-juan-pablo/550467).

La dinámica de las sesiones prácticas se gestionarán por el siguiente canal de [Discord](https://discord.gg/jS8FV3Fg).



### Distribución de sesiones de laboratorio

<div class="mt-schedule">
<style>
  .mt-schedule {
    font-family: 'Segoe UI', system-ui, -apple-system, sans-serif;
    max-width: 980px;
    margin: 2rem auto;
    padding: 0 1.25rem;
    color: #1e293b;
  }
  .mt-schedule h2 {
    text-align: center;
    font-size: 1.45rem;
    font-weight: 700;
    margin-bottom: 0.3rem;
    color: #0f172a;
  }
  .mt-schedule .mt-subtitle {
    text-align: center;
    color: #64748b;
    margin-bottom: 1.75rem;
    font-size: 0.88rem;
  }
  .mt-legend {
    display: flex;
    flex-wrap: wrap;
    gap: 0.6rem 1.4rem;
    background: #f8fafc;
    border: 1px solid #e2e8f0;
    border-radius: 10px;
    padding: 0.9rem 1.25rem;
    margin-bottom: 1.75rem;
    font-size: 0.8rem;
    color: #475569;
  }
  .mt-legend-item { display: flex; align-items: center; gap: 0.45rem; }
  .mt-legend-dot  { width: 13px; height: 13px; border-radius: 3px; flex-shrink: 0; }
  .mt-class {
    background: #fff;
    border: 1px solid #e2e8f0;
    border-radius: 14px;
    padding: 1.35rem 1.6rem 1.1rem;
    margin-bottom: 1.6rem;
    box-shadow: 0 2px 8px rgba(0,0,0,0.05);
  }
  .mt-class-header { display: flex; align-items: center; gap: 1rem; margin-bottom: 1.1rem; }
  .mt-badge {
    background: #1e40af;
    color: #fff;
    border-radius: 50%;
    width: 40px; height: 40px;
    display: flex; align-items: center; justify-content: center;
    font-weight: 700; font-size: 1rem; flex-shrink: 0;
  }
  .mt-class-title { font-size: 1.08rem; font-weight: 600; color: #1e3a8a; }
  .mt-class-meta  { font-size: 0.8rem; color: #64748b; margin-top: 0.15rem; }
  .mt-timeline {
    display: flex; height: 76px;
    border-radius: 8px; overflow: hidden;
    border: 1px solid rgba(0,0,0,0.07);
  }
  .mt-seg {
    display: flex; flex-direction: column;
    align-items: center; justify-content: center;
    color: #fff; font-size: 0.63rem; font-weight: 600;
    text-align: center; line-height: 1.3; padding: 2px 4px;
    cursor: default; transition: filter .15s;
    min-width: 0; overflow: hidden;
  }
  .mt-seg:hover { filter: brightness(0.87); }
  .mt-seg .lbl { overflow: hidden; max-width: 100%; white-space: nowrap; text-overflow: ellipsis; }
  .mt-seg .dur { font-size: 0.58rem; opacity: .82; font-weight: 400; margin-top: 3px; }
  .s-teoria  { background: #3b82f6; }
  .s-intro   { background: #0891b2; }
  .s-libre   { background: #16a34a; }
  .s-break   { background: #94a3b8; }
  .s-expo    { background: #ea580c; }
  .s-eval    { background: #7c3aed; }
  .mt-ruler  { position: relative; height: 24px; margin-top: 4px; }
  .mt-tick {
    position: absolute; font-size: 0.62rem; color: #94a3b8;
    transform: translateX(-50%); top: 6px; white-space: nowrap;
  }
  .mt-tick::before {
    content: '';
    display: block; width: 1px; height: 5px;
    background: #cbd5e1; margin: 0 auto 2px;
  }
  .mt-modal-b {
    display: flex; align-items: flex-start; gap: 0.5rem;
    font-size: 0.76rem; color: #166534;
    background: #f0fdf4; border: 1px solid #bbf7d0;
    border-radius: 7px; padding: 0.55rem 0.8rem; margin-top: 0.75rem;
  }
</style>

  <!-- LEYENDA -->
  <div class="mt-legend">
    <div class="mt-legend-item">
      <div class="mt-legend-dot" style="background:#3b82f6"></div>
      Teor&iacute;a / Repaso
    </div>
    <div class="mt-legend-item">
      <div class="mt-legend-dot" style="background:#0891b2"></div>
      Introducci&oacute;n Pr&aacute;ctica
    </div>
    <div class="mt-legend-item">
      <div class="mt-legend-dot" style="background:#16a34a"></div>
      Tiempo para hacer la pr&aacute;ctica
    </div>
    <div class="mt-legend-item">
      <div class="mt-legend-dot" style="background:#94a3b8"></div>
      Descanso
    </div>
    <div class="mt-legend-item">
      <div class="mt-legend-dot" style="background:#ea580c"></div>
      Exposici&oacute;n en directo
    </div>
    <div class="mt-legend-item">
      <div class="mt-legend-dot" style="background:#7c3aed"></div>
      Explicaci&oacute;n Evaluaci&oacute;n
    </div>
  </div>

  <!-- ============================================================
       CLASE 1: 16:00-20:00 (240 min)
       T1(30) | IntroP1(30) | Libre(60) | Break(30) | Libre(45) | Expo(30) | Eval1(15)
       %:     12.5   12.5    25           12.5         18.75       12.5       6.25
  ============================================================ -->
  <div class="mt-class">
    <div class="mt-class-header">
      <div class="mt-badge">1</div>
      <div>
        <div class="mt-class-title">Clase 1 &ndash; 7 de Mayo</div>
        <div class="mt-class-meta">16:00 &ndash; 20:00 &nbsp;&middot;&nbsp; 4 horas &nbsp;&middot;&nbsp; 1 descanso de 30 min</div>
      </div>
    </div>
    <div class="mt-timeline">
      <div class="mt-seg s-teoria"  style="width:12.5%"
           title="Introducci&oacute;n a la asignatura + Repaso T1 &middot; 16:00-16:30">
        <span class="lbl">Intro + T1</span>
        <span class="dur">16:00-16:30</span>
      </div>
      <div class="mt-seg s-intro"   style="width:12.5%"
           title="Introducci&oacute;n Pr&aacute;ctica 1 &middot; 16:30-17:00">
        <span class="lbl">Intro P1</span>
        <span class="dur">16:30-17:00</span>
      </div>
      <div class="mt-seg s-libre"   style="width:25%"
           title="Tiempo para hacer la pr&aacute;ctica P1 &middot; 17:00-18:00">
        <span class="lbl">Pr&aacute;ctica P1</span>
        <span class="dur">17:00-18:00</span>
      </div>
      <div class="mt-seg s-break"   style="width:12.5%"
           title="Descanso &middot; 18:00-18:30">
        <span class="lbl">Descanso</span>
        <span class="dur">18:00-18:30</span>
      </div>
      <div class="mt-seg s-libre"   style="width:18.75%"
           title="Tiempo para hacer la pr&aacute;ctica P1 &middot; 18:30-19:15">
        <span class="lbl">Pr&aacute;ctica P1</span>
        <span class="dur">18:30-19:15</span>
      </div>
      <div class="mt-seg s-expo"    style="width:12.5%"
           title="Exposici&oacute;n en directo &middot; 19:15-19:45">
        <span class="lbl">Expo Directo</span>
        <span class="dur">19:15-19:45</span>
      </div>
      <div class="mt-seg s-eval"    style="width:6.25%"
           title="Explicaci&oacute;n Evaluaci&oacute;n 1 &middot; 19:45-20:00">
        <span class="lbl">Eval 1</span>
        <span class="dur">19:45-20:00</span>
      </div>
    </div>
    <div class="mt-ruler">
      <span class="mt-tick" style="left:0%">16:00</span>
      <span class="mt-tick" style="left:12.5%">16:30</span>
      <span class="mt-tick" style="left:25%">17:00</span>
      <span class="mt-tick" style="left:50%">18:00</span>
      <span class="mt-tick" style="left:62.5%">18:30</span>
      <span class="mt-tick" style="left:81.25%">19:15</span>
      <span class="mt-tick" style="left:93.75%">19:45</span>
      <span class="mt-tick" style="left:100%">20:00</span>
    </div>
  </div>

  <!-- ============================================================
       CLASE 2: 16:00-21:00 (300 min)
       T2(30) | IntroP2(15) | Practica(35) | Break(30) | Practica(80) | Break(30) | Practica(20) | Expo(30) | Eval2(30)
       %:     10    5         11.67         10           26.67         10           6.66          10         10
  ============================================================ -->
  <div class="mt-class">
    <div class="mt-class-header">
      <div class="mt-badge">2</div>
      <div>
        <div class="mt-class-title">Clase 2 &ndash; 14 de Mayo</div>
        <div class="mt-class-meta">16:00 &ndash; 21:00 &nbsp;&middot;&nbsp; 5 horas &nbsp;&middot;&nbsp; 2 descansos de 30 min</div>
      </div>
    </div>
    <div class="mt-timeline">
      <div class="mt-seg s-teoria"  style="width:10%"
           title="Repaso Tema 2 &middot; 16:00-16:30">
        <span class="lbl">Repaso T2</span>
        <span class="dur">16:00-16:30</span>
      </div>
      <div class="mt-seg s-intro"   style="width:5%"
           title="Introducci&oacute;n Pr&aacute;ctica 2 &middot; 16:30-16:45">
        <span class="lbl">P2</span>
        <span class="dur">16:30-16:45</span>
      </div>
      <div class="mt-seg s-libre"   style="width:11.67%"
           title="Tiempo para hacer la pr&aacute;ctica P2 &middot; 16:45-17:20">
        <span class="lbl">Pr&aacute;ctica P2</span>
        <span class="dur">16:45-17:20</span>
      </div>
      <div class="mt-seg s-break"   style="width:10%"
           title="Descanso &middot; 17:20-17:50">
        <span class="lbl">Descanso</span>
        <span class="dur">17:20-17:50</span>
      </div>
      <div class="mt-seg s-libre"   style="width:26.67%"
           title="Tiempo para hacer la pr&aacute;ctica P2 &middot; 17:50-19:10">
        <span class="lbl">Pr&aacute;ctica P2</span>
        <span class="dur">17:50-19:10</span>
      </div>
      <div class="mt-seg s-break"   style="width:10%"
           title="Descanso &middot; 19:10-19:40">
        <span class="lbl">Descanso</span>
        <span class="dur">19:10-19:40</span>
      </div>
      <div class="mt-seg s-libre"   style="width:6.66%"
           title="Tiempo para hacer la pr&aacute;ctica P2 &middot; 19:40-20:00">
        <span class="lbl">Pr&aacute;ctica P2</span>
        <span class="dur">19:40-20:00</span>
      </div>
      <div class="mt-seg s-expo"    style="width:10%"
           title="Exposici&oacute;n en directo &middot; 20:00-20:30">
        <span class="lbl">Expo Directo</span>
        <span class="dur">20:00-20:30</span>
      </div>
      <div class="mt-seg s-eval"    style="width:10%"
           title="Explicaci&oacute;n Evaluaci&oacute;n 2 &middot; 20:30-21:00">
        <span class="lbl">Eval 2</span>
        <span class="dur">20:30-21:00</span>
      </div>
    </div>
    <div class="mt-ruler">
      <span class="mt-tick" style="left:0%">16:00</span>
      <span class="mt-tick" style="left:15%">16:45</span>
      <span class="mt-tick" style="left:26.67%">17:20</span>
      <span class="mt-tick" style="left:36.67%">17:50</span>
      <span class="mt-tick" style="left:63.33%">19:10</span>
      <span class="mt-tick" style="left:73.33%">19:40</span>
      <span class="mt-tick" style="left:80%">20:00</span>
      <span class="mt-tick" style="left:90%">20:30</span>
      <span class="mt-tick" style="left:100%">21:00</span>
    </div>
  </div>

  <!-- ============================================================
       CLASE 3: 16:00-21:00 (300 min)
       T3T4(30) | Práctica(50) | Break(30) | Práctica(80) | Break(30) | Práctica(50) | Expo(30)
       %:       10    16.67     10           26.67         10           16.67       10
  ============================================================ -->
  <div class="mt-class">
    <div class="mt-class-header">
      <div class="mt-badge">3</div>
      <div>
        <div class="mt-class-title">Clase 3 &ndash; 21 de Mayo</div>
        <div class="mt-class-meta">16:00 &ndash; 21:00 &nbsp;&middot;&nbsp; 5 horas &nbsp;&middot;&nbsp; 2 descansos de 30 min</div>
      </div>
    </div>
    <div class="mt-timeline">
      <div class="mt-seg s-teoria"  style="width:10%"
           title="Repaso Temas 3 y 4 &middot; 16:00-16:30">
        <span class="lbl">T3 + T4</span>
        <span class="dur">16:00-16:30</span>
      </div>
      <div class="mt-seg s-libre" style="width:16.67%"
           title="Tiempo para hacer la pr&aacute;ctica P3 &middot; 16:30-17:20">
        <span class="lbl">Pr&aacute;ctica P3</span>
        <span class="dur">16:30-17:20</span>
      </div>
      <div class="mt-seg s-break"   style="width:10%"
           title="Descanso &middot; 17:20-17:50">
        <span class="lbl">Descanso</span>
        <span class="dur">17:20-17:50</span>
      </div>
      <div class="mt-seg s-libre" style="width:26.67%"
           title="Tiempo para hacer la pr&aacute;ctica P3 &middot; 17:50-19:10">
        <span class="lbl">Pr&aacute;ctica P3</span>
        <span class="dur">17:50-19:10</span>
      </div>
      <div class="mt-seg s-break"   style="width:10%"
           title="Descanso &middot; 19:10-19:40">
        <span class="lbl">Descanso</span>
        <span class="dur">19:10-19:40</span>
      </div>
      <div class="mt-seg s-libre"   style="width:16.67%"
           title="Tiempo para hacer la pr&aacute;ctica P3 &middot; 19:40-20:30">
        <span class="lbl">Pr&aacute;ctica P3</span>
        <span class="dur">19:40-20:30</span>
      </div>
      <div class="mt-seg s-expo"    style="width:10%"
           title="Exposici&oacute;n en directo &middot; 20:30-21:00">
        <span class="lbl">Expo Directo</span>
        <span class="dur">20:30-21:00</span>
      </div>
    </div>
    <div class="mt-ruler">
      <span class="mt-tick" style="left:0%">16:00</span>
      <span class="mt-tick" style="left:10%">16:30</span>
      <span class="mt-tick" style="left:26.67%">17:20</span>
      <span class="mt-tick" style="left:36.67%">17:50</span>
      <span class="mt-tick" style="left:63.33%">19:10</span>
      <span class="mt-tick" style="left:73.33%">19:40</span>
      <span class="mt-tick" style="left:90%">20:30</span>
      <span class="mt-tick" style="left:100%">21:00</span>
    </div>
    <div class="mt-modal-b">
      &#9641; Durante el tiempo para hacer la pr&aacute;ctica se validar&aacute;n las ideas de la
      <strong>Evaluaci&oacute;n 2</strong>
    </div>
  </div>

</div>


## Temario

### Teoría

- [T1. Aplicaciones generales del PLN (areas generales)][t1]
- [T2. Aplicaciones específicas y Benchmacks][t2]
- [T2.1. Caso de estudio Análisis de Sentimientos][t2.1]
- [T3. Métricas de Evaluación][t3]
- [T4. Repositorios y Tecnologías de Modelos (Generativos) Preentrenados][t4]
<!--
% - [T5. AutoML. Descripción general y estado de la cuestión][t5]
% - [T5.1. AutoGOAL: Marco de trabajo para la generación de pipelines óptimos][t5.1]
-->

### Prácticas

- [P1. Creación de baseline con Sklearn. Caso de uso Clasificación de Documentos][p1] 
- [P1.2. Utilización de modelos transformers ya existentes como API. Caso de uso Clasificación de Documentos][p2]
% - [P2. Transformer fine-tunnig. Caso de uso Clasificación de Documentos][p3]
- [P2. Composición de características auxiliándose de transformers y otras tecnicas de extracción de  características. Caso de uso Clasificación de Documentos][p4]
- [P3. Modelos Generativos][p7]
- [P4. Consolidación de temario y trabajo en clase]()
<!--
   % - [P4. Ensembler de classificadores, entre ellos trasnformers, SMV, etc.  Caso de uso Clasificación  de Documentos][p5]
% - [P5. Utilización de técnicas de AutoML, libreria AutoGOAL.  Caso de uso Clasificación de Documentos][p6]
 -->


## Evaluación

### Teoría
 - [T1.C1. Cuestionario de evaluación](https://forms.gle/A9VANxkdBd99Ly5j9). Apertura el 20/03/2025- Cierre 23:59 del 26/03/2025.
 - [T2.C1. Cuestionario de evaluación](https://forms.gle/LKLfipcuPSk6J9qt6). Apertura el 27/03/2025- Cierre 23:59 del 02/04/2025.
 - [T2.1.C1. Cuestionario de evaluación](https://forms.gle/576ddPgDEfcrYmS1A). Apertura el 27/03/2025- Cierre 23:59 del 02/04/2025.
 - [T3.C1. Cuestionario de evaluación](https://forms.gle/DiDRZYNCHMxyumAp8). Apertura el 03/04/2025- Cierre 23:59 del 09/04/2025.
 - [T4.C1. Cuestionario de evaluación](https://forms.gle/St7f5jcVWgaczAgo6). Apertura el 10/04/2025- Cierre 23:59 del 07/05/2025.
<!--
 % - [T5.C1. Cuestionario de evaluación](https://forms.gle/G3AsHGFw4MXfMV2v9). Apertura el 15/03/2024- Cierre 23:59 del 17/04/2023.

% - [Cuestionario de setisfacción](https://forms.gle/sAobHzNaFSCu47ss8) 

-->
 

### Prácticas
 - P.Ev1. [Evaluación 1 (común)](https://jaspock.github.io/mtextos2425/bloque3_ev.html#entrega-1-comun). Apertura el 27/03/2025 - <strike>Cierre 23:59 del 10/04/2025</strike> Cierre 23:59 del 13/04/2025.
- P.Ev2. [Evaluación 2 (selectiva)](https://jaspock.github.io/mtextos2425/bloque3_ev.html#entrega-2-selectiva). Apertura el 10/04/2025 - Cierre 23:59 del 22/05/2025.
<!-- 
-->


### Utilidades
<!-- 
Gestión de créditos y máquinas virtuales con Google Colab: [Instrucciones](https://jaspock.github.io/mtextos2425/doc_utils/creditosColab/web.html)
-->
- Gestión de entornos Google Colab conectados a máquinas virtuales locales de Docker. [Instrucciones](https://jaspock.github.io/mtextos2425/doc_utils/colabEntornoLocal/web.html)


[abreu url]: https://scholar.google.es/citations?user=62u6KEkAAAAJ&hl=es
[javi url]: https://cvnet.cpd.ua.es/curriculum-breve/es/fernandez-martinez-javier/321
[yoan url]: https://cvnet.cpd.ua.es/curriculum-breve/es/gutierrez-vazquez-yoan/49618  

[t1]: https://jaspock.github.io/mtextos2425/bloque3_t1_aplicaciones.html
[t2]: https://jaspock.github.io/mtextos2425/bloque3_t2_subaplicaciones-benchmarks.html
[t2.1]: https://jaspock.github.io/mtextos2425/bloque3_t2.1_analisis_sentimientos.html
[t3]: https://jaspock.github.io/mtextos2425/bloque3_t3.1_metricas.html
[t4]: https://jaspock.github.io/mtextos2425/bloque3_t4_centralizacion.html
[t5]: https://jaspock.github.io/mtextos2425/bloque3_t5_automl.html
[t5.1]: https://jaspock.github.io/mtextos2425/bloque3_t5.1_autogoal.html

[p1]: https://jaspock.github.io/mtextos2425/bloque3_p1_SA-Pipeline-Reviews.html
[p2]: https://jaspock.github.io/mtextos2425/bloque3_p2_SA-Transformers-Basic.html
[p3]: https://jaspock.github.io/mtextos2425/bloque3_p3_SA-Transformers-Training-FineTuning.html
[p4]: https://jaspock.github.io/mtextos2425/bloque3_p4_SA-Transformers-Training-Custom.html
[p5]: https://jaspock.github.io/mtextos2425/bloque3_p5-SA-Ensemble.html
[p6]: https://jaspock.github.io/mtextos2425/bloque3_p6_SA-AutoGOAL.html
[p7]: https://jaspock.github.io/mtextos2425/bloque3_p6-SA-Generativos.html

[ev1]: https://jaspock.github.io/mtextos2425/bloque3_ev.html
