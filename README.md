
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Impressora Quântica 6D - Cenário 4: Doutor Manhattan / Nível Cósmico</title>
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        cosmic: {
                            bg: '#030712',
                            panel: 'rgba(10, 16, 35, 0.82)',
                            manhattan: '#00d8ff',
                            brana: '#a200ff',
                            gold: '#ffaa00',
                            void: '#010309',
                            border: 'rgba(0, 216, 255, 0.3)'
                        }
                    },
                    fontFamily: {
                        mono: ['Courier New', 'Consolas', 'monospace']
                    }
                }
            }
        }
    </script>
    <style>
        body {
            background-color: #030712;
            background-image: 
                radial-gradient(circle at 50% 15%, rgba(0, 216, 255, 0.08) 0%, transparent 60%),
                radial-gradient(circle at 85% 85%, rgba(162, 0, 255, 0.07) 0%, transparent 50%),
                radial-gradient(circle at 15% 75%, rgba(255, 170, 0, 0.05) 0%, transparent 45%),
                linear-gradient(to bottom, rgba(3, 7, 18, 0.95), rgba(1, 3, 9, 0.99));
            color: #e2e8f0;
            overflow-x: hidden;
        }

        /* Scrollbar Personalizada */
        ::-webkit-scrollbar { width: 6px; height: 6px; }
        ::-webkit-scrollbar-track { background: #010309; }
        ::-webkit-scrollbar-thumb { background: rgba(0, 216, 255, 0.4); border-radius: 3px; }
        ::-webkit-scrollbar-thumb:hover { background: rgba(0, 216, 255, 0.7); }

        /* HUD Futuristic Glassmorphic Card */
        .hud-card {
            background: rgba(10, 18, 36, 0.8);
            border: 1px solid rgba(0, 216, 255, 0.28);
            box-shadow: 0 8px 32px 0 rgba(0, 0, 0, 0.8), inset 0 0 20px rgba(0, 216, 255, 0.04);
            backdrop-filter: blur(12px);
            border-radius: 10px;
            position: relative;
        }
        .hud-card::before {
            content: '';
            position: absolute;
            top: 0; left: 0; width: 14px; height: 14px;
            border-top: 2px solid #00d8ff;
            border-left: 2px solid #00d8ff;
            border-top-left-radius: 8px;
        }
        .hud-card::after {
            content: '';
            position: absolute;
            bottom: 0; right: 0; width: 14px; height: 14px;
            border-bottom: 2px solid #a200ff;
            border-right: 2px solid #a200ff;
            border-bottom-right-radius: 8px;
        }

        .glow-manhattan { text-shadow: 0 0 12px rgba(0, 216, 255, 0.75); }
        .glow-brana { text-shadow: 0 0 12px rgba(162, 0, 255, 0.75); }
        .glow-gold { text-shadow: 0 0 12px rgba(255, 170, 0, 0.75); }

        .scanline-overlay {
            background: linear-gradient(
                to bottom,
                rgba(255,255,255,0),
                rgba(255,255,255,0) 50%,
                rgba(0, 216, 255, 0.03) 50%,
                rgba(0, 216, 255, 0.03)
            );
            background-size: 100% 4px;
            pointer-events: none;
        }

        input[type=range] {
            -webkit-appearance: none;
            background: #091224;
            border: 1px solid rgba(0, 216, 255, 0.3);
            height: 6px;
            border-radius: 3px;
        }
        input[type=range]::-webkit-slider-thumb {
            -webkit-appearance: none;
            height: 16px;
            width: 16px;
            border-radius: 50%;
            background: #00d8ff;
            box-shadow: 0 0 10px #00d8ff;
            cursor: pointer;
        }

        .pulse-cosmic {
            box-shadow: 0 0 0 0 rgba(0, 216, 255, 0.8);
            animation: pulse-cosmic 2s infinite;
        }
        @keyframes pulse-cosmic {
            0% { transform: scale(0.95); box-shadow: 0 0 0 0 rgba(0, 216, 255, 0.8); }
            70% { transform: scale(1); box-shadow: 0 0 0 12px rgba(0, 216, 255, 0); }
            100% { transform: scale(0.95); box-shadow: 0 0 0 0 rgba(0, 216, 255, 0); }
        }
    </style>
</head>
<body class="font-mono min-h-screen p-3 md:p-6 flex flex-col justify-between">

    <!-- HEADER / SUPERIOR STATUS -->
    <header class="w-full max-w-7xl mx-auto mb-4 border-b border-cosmic-border pb-4 flex flex-col md:flex-row justify-between items-center gap-4">
        <div>
            <div class="flex items-center gap-3">
                <div class="w-4 h-4 rounded-full bg-cosmic-manhattan pulse-cosmic"></div>
                <h1 class="text-xl md:text-2xl font-bold tracking-widest text-cosmic-manhattan glow-manhattan">
                    IMPRESSORA QUÂNTICA 6D <span class="text-xs font-normal text-cosmic-brana border border-cosmic-brana px-2 py-0.5 rounded">NÍVEL OMNIDIMENSIONAL</span>
                </h1>
            </div>
            <p class="text-xs text-slate-400 mt-1">Cenário 4: Transmutação de Matéria, Intangibilidade e Percepção Temporal Não-Linear (Doutor Manhattan / Capitã Marvel)</p>
        </div>
        
        <div class="flex items-center gap-3 text-xs">
            <div class="bg-slate-900/90 border border-cosmic-border px-3 py-1.5 rounded flex items-center gap-2">
                <span class="text-slate-400">ÂNCORA DE REALIDADE:</span>
                <span id="headerRealityAnchor" class="text-cosmic-manhattan font-bold">MATRIZ PRIMORDIAL (ONIVERSO)</span>
            </div>
            <div class="bg-slate-900/90 border border-cosmic-border px-3 py-1.5 rounded flex items-center gap-2">
                <span class="text-slate-400">FASE DA 6ª DIMENSÃO:</span>
                <span id="headerQuantumPhase" class="text-cosmic-gold font-bold">1.618034 (GOLDEN LOCK)</span>
            </div>
        </div>
    </header>

    <!-- VISÃO GERAL DO APLICATIVO / SUMMARY -->
    <section class="w-full max-w-7xl mx-auto mb-6">
        <div class="hud-card p-4 text-xs md:text-sm leading-relaxed text-slate-300">
            <div class="flex items-center justify-between border-b border-cosmic-border/40 pb-2 mb-3">
                <h2 class="text-cosmic-manhattan font-bold tracking-wider flex items-center gap-2">
                    <svg class="w-4 h-4 text-cosmic-manhattan" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 3v1m0 16v1m9-9h-1M4 12H3m15.364 6.364l-.707-.707M6.343 6.343l-.707-.707m12.728 0l-.707.707M6.343 17.657l-.707.707M16 12a4 4 0 11-8 0 4 4 0 018 0z"></path></svg>
                    VISÃO GERAL DO SISTEMA - REESTRUTURAÇÃO MACROSCÓPICA E OMNIDIMENSIONAL
                </h2>
                <span class="text-xs text-cosmic-gold font-semibold">FORA DO ESPAÇO-TEMPO CONVENCIONAL</span>
            </div>
            <div class="grid grid-cols-1 md:grid-cols-3 gap-4">
                <div>
                    <span class="text-cosmic-manhattan font-bold block mb-1">O QUE ACONTECE:</span>
                    <p class="text-slate-400">Transmutação instantânea de matéria, intangibilidade absoluta através de deslocamento de fase e percepção temporal simultânea de passado, presente e futuro.</p>
                </div>
                <div>
                    <span class="text-cosmic-brana font-bold block mb-1">MECANISMO DE OPERAÇÃO:</span>
                    <p class="text-slate-400">Aniquilação da matéria celular do operador e conversão em uma Função de Onda Macroscópica Consciente deslocalizada na Matriz Primordial de Membranas (Oniverso).</p>
                </div>
                <div>
                    <span class="text-cosmic-gold font-bold block mb-1">SINGULARIDADE DIRECTIONAL & SAMS:</span>
                    <p class="text-slate-400">Manipulação das constantes cosmológicas locais ($\Lambda$) e controle do transporte de Branas, permitindo projeção de avatares físicos e transmutações atômicas imediatas.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- WORKSPACE GRID -->
    <main class="w-full max-w-7xl mx-auto grid grid-cols-1 lg:grid-cols-12 gap-6 flex-grow">
        
        <!-- PAINEL DE CONTROLE LATERAL (4 COLUNAS) -->
        <div class="lg:col-span-4 flex flex-col gap-4">
            
            <!-- CONTROLES PRINCIPAIS DA SINGULARIDADE -->
            <div class="hud-card p-4 flex flex-col gap-3">
                <h3 class="text-xs font-bold text-cosmic-manhattan tracking-wider uppercase border-b border-cosmic-border/40 pb-2">
                    Mapeamento de Transmutação & Projeção
                </h3>
                
                <div class="grid grid-cols-1 gap-2">
                    <button id="btnDisintegrate" onclick="triggerDisintegration()" class="bg-cosmic-manhattan/10 hover:bg-cosmic-manhattan/20 text-cosmic-manhattan border border-cosmic-manhattan font-bold py-2.5 px-3 rounded text-xs transition duration-200 flex items-center justify-center gap-2">
                        <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z"></path></svg>
                        <span>DESINTEGRAR E RECIAR COMO FUNÇÃO DE ONDA</span>
                    </button>
                    
                    <button id="btnMultiverseTeleport" onclick="triggerMultiverseTeleport()" class="bg-cosmic-brana/20 hover:bg-cosmic-brana/30 text-cosmic-brana border border-cosmic-brana font-bold py-2.5 px-3 rounded text-xs transition duration-200 flex items-center justify-center gap-2">
                        <span>🌌 TELETRANSPORTE MULTIVERSAL (COLAPSO DE BRANA)</span>
                    </button>
                </div>

                <!-- CONTROLES TOGGLE DE SISTEMAS QUÂNTICOS -->
                <div class="grid grid-cols-1 gap-2 pt-1">
                    <button id="btnSingularity" onclick="toggleSingularityMechanism()" class="bg-cosmic-gold/10 hover:bg-cosmic-gold/20 text-cosmic-gold border border-cosmic-gold font-bold py-2 px-2 rounded text-xs transition duration-200 flex justify-between items-center">
                        <span>SINGULARIDADE DIRECIONADA:</span>
                        <span id="txtSingularityStatus" class="text-cosmic-manhattan">ATIVADA</span>
                    </button>
                    
                    <button id="btnSAMSDim" onclick="toggleSAMSDimensional()" class="bg-cosmic-brana/10 hover:bg-cosmic-brana/20 text-cosmic-brana border border-cosmic-brana font-bold py-2 px-2 rounded text-xs transition duration-200 flex justify-between items-center">
                        <span>SAMS DIMENSIONAL (BRANAS):</span>
                        <span id="txtSAMSStatus" class="text-cosmic-manhattan">SINCRONIZADO</span>
                    </button>
                </div>

                <!-- SELETOR DE TRANSMUTAÇÃO ATÔMICA -->
                <div class="pt-2 border-t border-cosmic-border/30">
                    <label class="text-slate-400 text-[11px] block mb-1">Transmutação Instantânea de Matéria:</label>
                    <select id="selectTransmutation" onchange="changeTransmutationMode(this.value)" class="w-full bg-slate-900 border border-cosmic-border text-cosmic-manhattan text-xs rounded p-2 focus:outline-none focus:border-cosmic-manhattan">
                        <option value="lead-gold">Chumbo (Pb 82) ➔ Ouro Purométrico (Au 79)</option>
                        <option value="flesh-energy">Carne Biológica ➔ Plasma Fotônico Puro</option>
                        <option value="darkmatter-photons">Matéria Escura ➔ Fótons Estelares</option>
                        <option value="quantum-vacuum">Flutuação de Vácuo ➔ Cristais de Hiperespaço</option>
                    </select>
                </div>
            </div>

            <!-- SLIDERS DE PARÂMETROS FÍSICOS DA REALIDADE -->
            <div class="hud-card p-4 flex flex-col gap-4">
                <h3 class="text-xs font-bold text-cosmic-gold tracking-wider uppercase border-b border-cosmic-border/40 pb-2">
                    Constantes do Espaço-Tempo
                </h3>

                <!-- Slider de Constante Cosmológica -->
                <div>
                    <div class="flex justify-between text-xs mb-1">
                        <span class="text-slate-400">Constante Cosmológica ($\Lambda$):</span>
                        <span id="valCosmoConstant" class="text-cosmic-manhattan font-bold">+1.20 x 10⁻⁵² m⁻²</span>
                    </div>
                    <input type="range" id="paramCosmoConstant" min="-100" max="100" value="12" class="w-full" oninput="updateParam('cosmo', this.value)">
                </div>

                <!-- Slider de Dimensão de Ancoragem -->
                <div>
                    <div class="flex justify-between text-xs mb-1">
                        <span class="text-slate-400">Dimensão de Ancoragem (3D a 6D):</span>
                        <span id="valAnchorDim" class="text-cosmic-brana font-bold">6.0D (Hiperespaço)</span>
                    </div>
                    <input type="range" id="paramAnchorDim" min="30" max="60" value="60" class="w-full" oninput="updateParam('dimension', this.value)">
                </div>

                <!-- Slider de Frequência de Fase Quântica -->
                <div>
                    <div class="flex justify-between text-xs mb-1">
                        <span class="text-slate-400">Frequência de Fase da 6ª Dimensão:</span>
                        <span id="valPhaseFreq" class="text-cosmic-gold font-bold">432.0 THz</span>
                    </div>
                    <input type="range" id="paramPhaseFreq" min="100" max="1000" value="432" class="w-full" oninput="updateParam('phase', this.value)">
                </div>
            </div>

            <!-- DIAGNÓSTICOS DO CORPO / ESTADO CÓSMICO -->
            <div class="hud-card p-4 flex flex-col gap-3">
                <h3 class="text-xs font-bold text-cosmic-brana tracking-wider uppercase border-b border-cosmic-border/40 pb-2">
                    Métricas de Existência Onipresente
                </h3>

                <!-- Entropia Gauge Bar -->
                <div>
                    <div class="flex justify-between text-xs mb-1">
                        <span class="text-slate-400">Entropia Local do Espaço-Tempo:</span>
                        <span id="valEntropyPercent" class="text-cosmic-manhattan font-bold">0.001 % (Zero Absoluto)</span>
                    </div>
                    <div class="w-full bg-slate-900 h-3 rounded border border-cosmic-border/50 overflow-hidden relative">
                        <div id="barEntropy" class="bg-gradient-to-r from-cosmic-manhattan via-cosmic-brana to-cosmic-gold h-full transition-all duration-300" style="width: 5%"></div>
                    </div>
                </div>

                <div class="grid grid-cols-2 gap-2 text-xs pt-2">
                    <div class="bg-slate-900/80 p-2 rounded border border-slate-800">
                        <span class="text-slate-400 block text-[10px]">ESTADO CORPORAL</span>
                        <span id="metricBodyState" class="text-cosmic-manhattan text-sm font-bold">ONDA CONSCIENTE</span>
                    </div>
                    <div class="bg-slate-900/80 p-2 rounded border border-slate-800">
                        <span class="text-slate-400 block text-[10px]">DENSIDADE DA BRANA</span>
                        <span id="metricBraneDensity" class="text-cosmic-brana text-sm font-bold">1.414 Planck</span>
                    </div>
                    <div class="bg-slate-900/80 p-2 rounded border border-slate-800">
                        <span class="text-slate-400 block text-[10px]">INVARIÂNCIA TEMPORAL</span>
                        <span id="metricTimeInvariance" class="text-cosmic-gold text-sm font-bold">NÃO-LINEAR (∞)</span>
                    </div>
                    <div class="bg-slate-900/80 p-2 rounded border border-slate-800">
                        <span class="text-slate-400 block text-[10px]">NÍVEL DA REALIDADE</span>
                        <span id="metricRealityLevel" class="text-cosmic-manhattan text-sm font-bold">MATRIZ PRIMORDIAL</span>
                    </div>
                </div>
            </div>

        </div>

        <!-- COLUNA DIREITA: VISUALIZADOR CANVAS 2D & TERMINAL DE LOGS (8 COLUNAS) -->
        <div class="lg:col-span-8 flex flex-col gap-4">
            
            <!-- CANVAS CONTAINER -->
            <div class="hud-card p-2 relative flex flex-col items-center justify-center min-h-[480px] md:min-h-[540px]">
                
                <!-- HUD Overlays de Informação no Visor Canvas -->
                <div class="absolute top-4 left-4 z-10 pointer-events-none text-[11px] text-cosmic-manhattan/90 flex flex-col gap-1">
                    <div>VISOR CÓSMICO: SIMULAÇÃO MACROSCÓPICA 6D</div>
                    <div class="text-slate-400 text-[10px]">ENTRELAÇAMENTO • AVATAR PROJETADO • ONDAS DE GRAVIDADE</div>
                </div>

                <div class="absolute top-4 right-4 z-10 pointer-events-none text-right text-[11px]">
                    <div id="hudWaveState" class="font-bold text-cosmic-manhattan">SISTEMA: FUNÇÃO DE ONDA INTEGRADA</div>
                    <div id="hudParticleCount" class="text-slate-400 text-[10px]">Partículas Entrelaçadas: 12,400</div>
                </div>

                <!-- Botões de Troca de Modo de Visualização do Canvas -->
                <div class="absolute bottom-4 left-4 z-10 flex flex-wrap gap-2">
                    <button onclick="setViewMode('wave')" class="bg-slate-900/80 border border-cosmic-border text-slate-300 text-[10px] px-2.5 py-1 rounded hover:bg-cosmic-manhattan/20">COLAPSO DE ONDA</button>
                    <button onclick="setViewMode('brane')" class="bg-slate-900/80 border border-cosmic-border text-slate-300 text-[10px] px-2.5 py-1 rounded hover:bg-cosmic-manhattan/20">TEIA DE BRANAS</button>
                    <button onclick="setViewMode('transmutation')" class="bg-slate-900/80 border border-cosmic-border text-slate-300 text-[10px] px-2.5 py-1 rounded hover:bg-cosmic-manhattan/20">TRANSMUTAÇÃO</button>
                    <button onclick="setViewMode('timeline')" class="bg-slate-900/80 border border-cosmic-border text-slate-300 text-[10px] px-2.5 py-1 rounded hover:bg-cosmic-manhattan/20">LINHA DO TEMPO NÃO-LINEAR</button>
                </div>

                <!-- Canvas Principal Interativo -->
                <canvas id="canvasCosmic6D" class="w-full h-full rounded cursor-pointer scanline-overlay"></canvas>
            </div>

            <!-- TERMINAL DE REGISTRO E LOGS CÓSMICOS -->
            <div class="hud-card p-4 flex flex-col gap-2">
                <div class="flex justify-between items-center border-b border-cosmic-border/40 pb-2">
                    <h3 class="text-xs font-bold text-cosmic-manhattan tracking-wider uppercase flex items-center gap-2">
                        <span class="w-2 h-2 rounded-full bg-cosmic-manhattan animate-ping"></span>
                        Terminal de Eventos Cosmológicos e Colapsos de Brana
                    </h3>
                    <button onclick="clearLogs()" class="text-[10px] text-slate-400 hover:text-cosmic-manhattan">LIMPAR LOGS</button>
                </div>
                
                <div id="telemetryLog" class="bg-slate-950/80 border border-slate-800/80 rounded p-3 h-32 overflow-y-auto font-mono text-[11px] leading-relaxed flex flex-col gap-1">
                    <div class="text-slate-500">[00:00:00] Inicializando sistema omnidimensional para simulação de Função de Onda Consciente...</div>
                    <div class="text-cosmic-manhattan">[00:00:01] Matriz Primordial ancorada. Consciência deslocalizada no Oniverso.</div>
                </div>
            </div>

        </div>

    </main>

    <!-- FOOTER -->
    <footer class="w-full max-w-7xl mx-auto mt-6 pt-4 border-t border-cosmic-border/30 text-center text-xs text-slate-500 flex flex-col md:flex-row justify-between items-center gap-2">
        <div>Simulação Biocósmica Quântica - Cenário Doutor Manhattan / Capitã Marvel</div>
        <div>Tecnologia: HTML5 Canvas 2D | Tailwind CSS | Mecanismo de Singularidade Direcionada</div>
    </footer>

    <!-- LOGICA JAVASCRIPT -->
    <script>
        // =========================================================================
        // GERENCIAMENTO DE ESTADO GLOBAL E VARIÁVEIS CÓSMICAS
        // =========================================================================
        const canvas = document.getElementById('canvasCosmic6D');
        const ctx = canvas.getContext('2d');

        let isSingularityActive = true;
        let isSAMSSynced = true;
        let viewMode = 'wave'; // 'wave', 'brane', 'transmutation', 'timeline'
        let transmutationType = 'lead-gold';

        let phaseTime = 0;
        let isDisintegrated = true; // Por padrão já opera como função de onda consciente
        let teleportFlash = 0;

        // Parâmetros do Espaço-Tempo
        const params = {
            cosmoConstant: 1.20,
            anchorDimension: 6.0,
            phaseFreq: 432
        };

        // Entidades de Partículas e Nós de Brana
        let quantumParticles = [];
        let braneGridNodes = [];
        let shockwaves = [];
        let timelineLoops = [];

        function resizeCanvas() {
            const container = canvas.parentElement;
            canvas.width = container.clientWidth - 16;
            canvas.height = container.clientHeight - 16;
            initBraneGrid();
            initTimelineLoops();
        }
        window.addEventListener('resize', resizeCanvas);

        // =========================================================================
        // INICIALIZAÇÃO DE ELEMENTOS VISUAIS
        // =========================================================================
        function initBraneGrid() {
            braneGridNodes = [];
            const cols = 14;
            const rows = 10;
            const spacingX = canvas.width / (cols + 1);
            const spacingY = canvas.height / (rows + 1);

            for (let r = 0; r < rows; r++) {
                for (let c = 0; c < cols; c++) {
                    braneGridNodes.push({
                        x: (c + 1) * spacingX,
                        y: (r + 1) * spacingY,
                        baseX: (c + 1) * spacingX,
                        baseY: (r + 1) * spacingY,
                        phase: Math.random() * Math.PI * 2
                    });
                }
            }
        }

        function initTimelineLoops() {
            timelineLoops = [];
            for (let i = 0; i < 5; i++) {
                timelineLoops.push({
                    radius: 40 + i * 35,
                    speed: (i % 2 === 0 ? 1 : -1) * (0.01 + i * 0.005),
                    angle: Math.random() * Math.PI * 2,
                    label: i === 0 ? 'Passado Absoluto' : i === 1 ? 'Presente Estacionário' : i === 2 ? 'Futuro Probabilístico' : `Hiperespaço T+${i}`
                });
            }
        }

        // População de partículas de Função de Onda Quântica
        for (let i = 0; i < 180; i++) {
            quantumParticles.push({
                x: Math.random() * 800,
                y: Math.random() * 600,
                vx: (Math.random() - 0.5) * 1.5,
                vy: (Math.random() - 0.5) * 1.5,
                radius: Math.random() * 3 + 1,
                color: Math.random() > 0.4 ? '#00d8ff' : Math.random() > 0.5 ? '#a200ff' : '#ffaa00',
                orbitAngle: Math.random() * Math.PI * 2,
                orbitSpeed: 0.01 + Math.random() * 0.03
            });
        }

        // =========================================================================
        // MÉTODOS AUXILIARES DE LOG
        // =========================================================================
        function logTelemetry(msg, type = 'info') {
            const logBox = document.getElementById('telemetryLog');
            const time = new Date().toTimeString().split(' ')[0];
            const div = document.createElement('div');
            
            let colorClass = 'text-slate-300';
            if (type === 'manhattan') colorClass = 'text-cosmic-manhattan';
            if (type === 'brana') colorClass = 'text-cosmic-brana';
            if (type === 'gold') colorClass = 'text-cosmic-gold';
            if (type === 'crimson') colorClass = 'text-red-400';

            div.className = colorClass;
            div.innerHTML = `<span class="text-slate-500">[${time}]</span> ${msg}`;
            logBox.appendChild(div);
            logBox.scrollTop = logBox.scrollHeight;
        }

        function clearLogs() {
            document.getElementById('telemetryLog').innerHTML = '';
            logTelemetry('Registros cosmológicos limpos.', 'info');
        }

        // =========================================================================
        // CONTROLES DE INTERAÇÃO E AÇÕES
        // =========================================================================
        function triggerDisintegration() {
            isDisintegrated = !isDisintegrated;
            const btn = document.getElementById('btnDisintegrate');

            if (isDisintegrated) {
                btn.innerHTML = `<span>DESINTEGRAR E RECREAR COMO FUNÇÃO DE ONDA</span>`;
                logTelemetry('⚡ Aniquilação Subatômica executada! Corpo biológico desintegrado e projetado como Função de Onda Consciente na Matriz Primordial.', 'manhattan');
            } else {
                btn.innerHTML = `<span>CONDENSAR NÚCLEO FÍSICO TEMPORÁRIO</span>`;
                logTelemetry('⚠️ Função de onda condensada temporariamente em um chassi físico tridimensional local.', 'gold');
            }

            // Disparar onda de choque gravitacional
            shockwaves.push({
                x: canvas.width / 2,
                y: canvas.height / 2,
                radius: 10,
                maxRadius: canvas.width * 0.8,
                alpha: 1.0,
                color: '#00d8ff'
            });
        }

        function triggerMultiverseTeleport() {
            teleportFlash = 1.0;
            logTelemetry('🌌 Teletransporte Multiversal ativado! Desconexão de fase da brana atual e reconexão em novas coordenadas do Oniverso.', 'brana');

            // Repor partículas
            quantumParticles.forEach(p => {
                p.x = Math.random() * canvas.width;
                p.y = Math.random() * canvas.height;
            });

            shockwaves.push({
                x: canvas.width / 2,
                y: canvas.height / 2,
                radius: 10,
                maxRadius: canvas.width,
                alpha: 1.0,
                color: '#a200ff'
            });
        }

        function toggleSingularityMechanism() {
            isSingularityActive = !isSingularityActive;
            const txt = document.getElementById('txtSingularityStatus');
            txt.textContent = isSingularityActive ? 'ATIVADA' : 'DESATIVADA';
            txt.className = isSingularityActive ? 'text-cosmic-manhattan' : 'text-red-400';
            logTelemetry(`Mecanismo de Singularidade Direcionada: ${isSingularityActive ? 'ATIVADO' : 'INATIVO'}.`, isSingularityActive ? 'manhattan' : 'crimson');
        }

        function toggleSAMSDimensional() {
            isSAMSSynced = !isSAMSSynced;
            const txt = document.getElementById('txtSAMSStatus');
            txt.textContent = isSAMSSynced ? 'SINCRONIZADO' : 'FORA DE FASE';
            txt.className = isSAMSSynced ? 'text-cosmic-manhattan' : 'text-red-400';
            logTelemetry(`SAMS Dimensional (Matriz de Branas): ${isSAMSSynced ? 'SINCRONIZADO' : 'DESINCRONIZADO'}.`, isSAMSSynced ? 'brana' : 'crimson');
        }

        function changeTransmutationMode(val) {
            transmutationType = val;
            let label = '';
            if (val === 'lead-gold') label = 'Chumbo (Pb) ➔ Ouro Purométrico (Au)';
            if (val === 'flesh-energy') label = 'Carne Biológica ➔ Plasma Fotônico';
            if (val === 'darkmatter-photons') label = 'Matéria Escura ➔ Fótons Estelares';
            if (val === 'quantum-vacuum') label = 'Vácuo Quântico ➔ Cristais de Hiperespaço';

            logTelemetry(`Matriz de Transmutação alterada para: ${label}`, 'gold');
        }

        function setViewMode(mode) {
            viewMode = mode;
            let modeName = '';
            if (mode === 'wave') modeName = 'COLAPSO DE FUNÇÃO DE ONDA';
            if (mode === 'brane') modeName = 'TEIA DE BRANAS MULTIVERSAL';
            if (mode === 'transmutation') modeName = 'MATRIZ DE TRANSMUTAÇÃO ATÔMICA';
            if (mode === 'timeline') modeName = 'LINHA DO TEMPO NÃO-LINEAR';

            logTelemetry(`Modo de visualização alterado para: ${modeName}`, 'manhattan');
        }

        function updateParam(type, val) {
            if (type === 'cosmo') {
                params.cosmoConstant = (parseFloat(val) / 10).toFixed(2);
                document.getElementById('valCosmoConstant').textContent = `${params.cosmoConstant > 0 ? '+' : ''}${params.cosmoConstant} x 10⁻⁵² m⁻²`;
            } else if (type === 'dimension') {
                params.anchorDimension = (parseFloat(val) / 10).toFixed(1);
                document.getElementById('valAnchorDim').textContent = `${params.anchorDimension}D (${params.anchorDimension >= 5 ? 'Hiperespaço' : 'Espaço Convencional'})`;
            } else if (type === 'phase') {
                params.phaseFreq = parseInt(val);
                document.getElementById('valPhaseFreq').textContent = `${params.phaseFreq}.0 THz`;
            }
        }

        // =========================================================================
        // ATUALIZAÇÃO DA SIMULAÇÃO E RENDERIZAÇÃO
        // =========================================================================
        function updateSimulation() {
            phaseTime += 0.03;

            // Decaimento do Flash de Teletransporte
            if (teleportFlash > 0) teleportFlash -= 0.03;

            // Movimentação de Partículas Quânticas
            const centerX = canvas.width / 2;
            const centerY = canvas.height / 2;

            quantumParticles.forEach(p => {
                p.orbitAngle += p.orbitSpeed * (params.phaseFreq / 400);

                if (isDisintegrated) {
                    // Orbitar ao redor do centro gravitacional consciente
                    const targetX = centerX + Math.cos(p.orbitAngle) * (120 + Math.sin(phaseTime) * 30);
                    const targetY = centerY + Math.sin(p.orbitAngle) * (120 + Math.cos(phaseTime) * 30);
                    p.x += (targetX - p.x) * 0.05;
                    p.y += (targetY - p.y) * 0.05;
                } else {
                    // Dispersão livre
                    p.x += p.vx;
                    p.y += p.vy;
                    if (p.x < 0 || p.x > canvas.width) p.vx *= -1;
                    if (p.y < 0 || p.y > canvas.height) p.vy *= -1;
                }
            });

            // Atualização de Ondas de Choque Gravitacionais
            shockwaves.forEach((sw, idx) => {
                sw.radius += 12;
                sw.alpha -= 0.015;
                if (sw.alpha <= 0) shockwaves.splice(idx, 1);
            });

            // Atualizar UI Status
            document.getElementById('metricBodyState').textContent = isDisintegrated ? 'ONDA CONSCIENTE' : 'NÚCLEO CONDENSADO';
            document.getElementById('hudWaveState').textContent = isDisintegrated ? 'SISTEMA: FUNÇÃO DE ONDA MACROSCÓPICA ATIVA' : 'SISTEMA: CORPO RECONSTITUÍDO LOCALMENTE';
            document.getElementById('valEntropyPercent').textContent = `${(0.001 * (10.1 - params.anchorDimension)).toFixed(4)} %`;
        }

        // =========================================================================
        // DESENHO NO CANVAS 2D
        // =========================================================================
        function drawGrid() {
            ctx.strokeStyle = 'rgba(0, 216, 255, 0.04)';
            ctx.lineWidth = 1;
            const gridSize = 35;

            for (let x = 0; x < canvas.width; x += gridSize) {
                ctx.beginPath();
                ctx.moveTo(x, 0);
                ctx.lineTo(x, canvas.height);
                ctx.stroke();
            }
            for (let y = 0; y < canvas.height; y += gridSize) {
                ctx.beginPath();
                ctx.moveTo(0, y);
                ctx.lineTo(canvas.width, y);
                ctx.stroke();
            }
        }

        function drawWaveView(centerX, centerY) {
            // Desenhar Avatar Projetado por Partículas Entrelaçadas (Simbolismo de Doutor Manhattan / Energia)
            ctx.save();
            ctx.translate(centerX, centerY);

            // Anéis de Fase Multidimensionais
            for (let i = 1; i <= 3; i++) {
                ctx.beginPath();
                ctx.ellipse(0, 0, i * 65, i * 35, phaseTime * (i % 2 === 0 ? 1 : -1), 0, Math.PI * 2);
                ctx.strokeStyle = i === 1 ? 'rgba(0, 216, 255, 0.5)' : i === 2 ? 'rgba(162, 0, 255, 0.4)' : 'rgba(255, 170, 0, 0.3)';
                ctx.lineWidth = 1.5;
                ctx.stroke();
            }

            // Símbolo do Átomo de Hidrogênio / Núcleo Consciente no Centro
            ctx.beginPath();
            ctx.arc(0, 0, 18, 0, Math.PI * 2);
            ctx.fillStyle = '#00d8ff';
            ctx.shadowColor = '#00d8ff';
            ctx.shadowBlur = 25;
            ctx.fill();

            ctx.beginPath();
            ctx.arc(0, 0, 8, 0, Math.PI * 2);
            ctx.fillStyle = '#ffffff';
            ctx.fill();
            ctx.shadowBlur = 0;

            ctx.restore();
        }

        function drawBraneTeia() {
            ctx.lineWidth = 1;

            braneGridNodes.forEach((node, i) => {
                const offsetX = Math.sin(phaseTime + node.phase) * 12;
                const offsetY = Math.cos(phaseTime + node.phase) * 12;
                const currX = node.baseX + offsetX;
                const currY = node.baseY + offsetY;

                // Conectar nós adjacentes para formar a membrana de Branas
                braneGridNodes.forEach((neighbor, j) => {
                    if (i < j) {
                        const dist = Math.hypot(currX - neighbor.baseX, currY - neighbor.baseY);
                        if (dist < 80) {
                            ctx.beginPath();
                            ctx.moveTo(currX, currY);
                            ctx.lineTo(neighbor.baseX, neighbor.baseY);
                            ctx.strokeStyle = `rgba(162, 0, 255, ${0.4 - dist / 200})`;
                            ctx.stroke();
                        }
                    }
                });

                // Nó da Brana
                ctx.beginPath();
                ctx.arc(currX, currY, 3, 0, Math.PI * 2);
                ctx.fillStyle = '#a200ff';
                ctx.shadowColor = '#a200ff';
                ctx.shadowBlur = 6;
                ctx.fill();
                ctx.shadowBlur = 0;
            });
        }

        function drawTransmutationMatrix(centerX, centerY) {
            ctx.save();
            ctx.translate(centerX, centerY);

            const numAtoms = 12;
            const radius = 140;

            for (let i = 0; i < numAtoms; i++) {
                const angle = (i / numAtoms) * Math.PI * 2 + phaseTime;
                const x = Math.cos(angle) * radius;
                const y = Math.sin(angle) * radius;

                // Raios de Transmutação
                ctx.beginPath();
                ctx.moveTo(0, 0);
                ctx.lineTo(x, y);
                ctx.strokeStyle = 'rgba(255, 170, 0, 0.4)';
                ctx.lineWidth = 1.5;
                ctx.stroke();

                // Átomos Transmutados
                ctx.beginPath();
                ctx.arc(x, y, 10, 0, Math.PI * 2);
                ctx.fillStyle = i % 2 === 0 ? '#ffaa00' : '#00d8ff';
                ctx.shadowColor = ctx.fillStyle;
                ctx.shadowBlur = 12;
                ctx.fill();
            }

            ctx.restore();
        }

        function drawTimelineView(centerX, centerY) {
            ctx.save();
            ctx.translate(centerX, centerY);

            timelineLoops.forEach(loop => {
                loop.angle += loop.speed;

                // Anel Temporal
                ctx.beginPath();
                ctx.arc(0, 0, loop.radius, 0, Math.PI * 2);
                ctx.strokeStyle = 'rgba(0, 216, 255, 0.3)';
                ctx.lineWidth = 1.5;
                ctx.stroke();

                // Marcador Temporal Simultâneo
                const px = Math.cos(loop.angle) * loop.radius;
                const py = Math.sin(loop.angle) * loop.radius;

                ctx.beginPath();
                ctx.arc(px, py, 6, 0, Math.PI * 2);
                ctx.fillStyle = '#ffaa00';
                ctx.shadowColor = '#ffaa00';
                ctx.shadowBlur = 10;
                ctx.fill();

                // Rótulo Temporal
                ctx.fillStyle = '#e2e8f0';
                ctx.font = '9px monospace';
                ctx.fillText(loop.label, px + 10, py + 3);
            });

            ctx.restore();
        }

        function render() {
            ctx.clearRect(0, 0, canvas.width, canvas.height);

            const centerX = canvas.width / 2;
            const centerY = canvas.height / 2;

            drawGrid();

            // Renderização do Modo Escolhido
            if (viewMode === 'wave') {
                drawWaveView(centerX, centerY);
            } else if (viewMode === 'brane') {
                drawBraneTeia();
            } else if (viewMode === 'transmutation') {
                drawTransmutationMatrix(centerX, centerY);
            } else if (viewMode === 'timeline') {
                drawTimelineView(centerX, centerY);
            }

            // Renderizar Partículas Quânticas Globais
            quantumParticles.forEach(p => {
                ctx.beginPath();
                ctx.arc(p.x, p.y, p.radius, 0, Math.PI * 2);
                ctx.fillStyle = p.color;
                ctx.shadowColor = p.color;
                ctx.shadowBlur = 8;
                ctx.fill();
                ctx.shadowBlur = 0;
            });

            // Renderizar Ondas de Choque
            shockwaves.forEach(sw => {
                ctx.beginPath();
                ctx.arc(sw.x, sw.y, sw.radius, 0, Math.PI * 2);
                ctx.strokeStyle = sw.color;
                ctx.globalAlpha = sw.alpha;
                ctx.lineWidth = 3;
                ctx.stroke();
                ctx.globalAlpha = 1.0;
            });

            // Effect Flash Teletransporte Multiversal
            if (teleportFlash > 0) {
                ctx.fillStyle = `rgba(162, 0, 255, ${teleportFlash})`;
                ctx.fillRect(0, 0, canvas.width, canvas.height);
            }

            updateSimulation();
            requestAnimationFrame(render);
        }

        // Interatividade por Clique no Canvas: Projetar Avatar / Colapso de Transmutação
        canvas.addEventListener('click', (e) => {
            const rect = canvas.getBoundingClientRect();
            const clickX = e.clientX - rect.left;
            const clickY = e.clientY - rect.top;

            shockwaves.push({
                x: clickX,
                y: clickY,
                radius: 5,
                maxRadius: 200,
                alpha: 1.0,
                color: '#ffaa00'
            });

            // Atrair partículas para as coordenadas do clique
            quantumParticles.forEach(p => {
                p.x = clickX + (Math.random() - 0.5) * 60;
                p.y = clickY + (Math.random() - 0.5) * 60;
            });

            logTelemetry(`⚡ Projeção de Avatar / Colapso de Transmutação executado nas coordenadas (${Math.round(clickX)}, ${Math.round(clickY)}).`, 'gold');
        });

        // =========================================================================
        // CARREGAMENTO INICIAL
        // =========================================================================
        window.onload = () => {
            resizeCanvas();
            logTelemetry('Sistema omnidimensional do Cenário 4 (Doutor Manhattan) totalmente carregado.', 'manhattan');
            logTelemetry('Função de Onda Consciente ancorada na Matriz Primordial (Oniverso).', 'brana');
            render();
        };
    </script>
</body>
</html>
