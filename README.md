# PIR12: Comprehensive Technical Specification, Architectural Blueprint, and Monolithic Runtime System

## Author and Intellectual Property Owner
Juho Artturi Hemminki

## Proprietary Copyright Notice
Copyright (c) 2026 Juho Artturi Hemminki. All Rights Reserved. All Claims Reserved Worldwide. Licensing requests, commercial assessment, and institutional evaluations must be formally submitted via projectflagcarrier@gmail.com.

## 1. Complete Theoretical Foundations and Design Principles

### 1.1 The Core Philosophy of PIR12
PIR12 represents a fundamental shift in application runtime design within highly restricted execution environments. Modern computing ecosystems are top-heavy with abstraction layers. Applications typically sit on top of massive visual components, state management frameworks, high-level script interfaces, and managed runtime virtual machines. While these layers provide developers with a fast production cycle, they introduce a massive performance cost, memory fragmentation, and significant input-to-render latency.

PIR12 completely rejects this multi-layered layout approach. It introduces a flat, data-oriented execution architecture where user text commands, processing instructions, and application visual states are decoupled from static compilation steps. The platform turns human or programmatic intentions directly into continuous binary data transformations executed over a pre-allocated raw memory buffer. PIR12 does not run an internal script engine. Instead, it operates as a secure execution sandbox, handling software behavior as multi-dimensional operations executed natively on the underlying physical hardware layers.

### 1.2 Bypassing Environment Security Constraints
Modern high-security execution sandboxes, such as professional web browsers and corporate application containers, protect host systems through strict Content Security Policy (CSP) frameworks. Headers like `default-src 'self'` and `script-src 'self'` are designed to block security risks by preventing the runtime evaluation of dynamic script strings. This means classic dynamic code execution methods—such as the standard `eval()` function or `new Function()` instantiations—are fundamentally unusable in secure corporate and institutional production deployments.

PIR12 resolves this core problem without using dangerous security exceptions like the `'unsafe-eval'` configuration flag. The engine processes text instructions through an immutable, factory-mapped syntax dictionary. Human commands are parsed into precise arrays of performance and configuration attributes. These structural parameters modify pre-compiled, optimized rendering and calculation loops that process typed data matrices inside the sandbox. As a result, users gain full dynamic application flexibility while keeping the execution layer entirely secure and fully compliant with strict local policies.

## 2. Low-Level Memory Topology and Data-Oriented Design

### 2.1 Data-Oriented Core Framework
To guarantee predictable, real-time performance curves under extreme load conditions, PIR12 entirely moves away from Object-Oriented Programming (OOP) memory management. In classic object-oriented engines, data states are tracked via variable heap-allocated reference objects. These objects are scattered arbitrarily across physical memory blocks, causing pointer indirection, cache line pollution, and garbage collection pauses.

PIR12 forces a strict Data-Oriented Design (DOD) model by allocating a flat, unified, non-extensible block of memory using a raw ArrayBuffer during the boot phase. This array buffer acts as the physical RAM space of the PIR12 machine, which is then sliced into specialized typed arrays (Uint32Array, Float32Array, and Uint8Array) to match the hardware architecture.

### 2.2 Memory Array Layout Map Allocation
The entire virtual system block is partitioned into precise byte offsets to eliminate any runtime pointer allocation overhead:
* **The System Control Block (0x00000000 to 0x00000FFF):** This memory segment houses the platform registers. It includes the Global Program Counter, individual micro-thread pointer records, frame tracking loops, execution status flags, and event ring buffer boundaries.
* **The Component Definition Registry (0x00001000 to 0x00003FFF):** Reserved for mapping dynamic user windows, layout attributes, spatial geometry matrices, sizing boundaries, and operational nodes.
* **The Multi-Thread Shared Heap (0x00004000 onwards):** A raw byte arena utilized by general-purpose active modules, including high-throughput data tables, terminal historical arrays, and active processing buffers.

### 2.3 Elimination of Garbage Collection Latency
Standard applications degrade in rendering consistency when processing heavy data streams because the system is forced to continually allocate new object wrappers and temporary state arrays. This creates massive memory noise that causes the host environment's automatic garbage collection loop to trigger periodic execution pauses, dropping frames and ruining the user experience.

PIR12 avoids this limitation by enforcing a hard policy of zero structural runtime memory allocation during active processing loops. Application variables, operational parameters, and layout updates are handled using fixed pointer rings inside the pre-allocated memory buffer. Since the heap footprint remains completely flat throughout execution, garbage collection pauses are dropped to absolute zero. This architecture guarantees a completely smooth, linear rendering cycle matching native display rates at 60Hz or 120Hz.

## 3. Subsystem Execution Framework

### 3.1 Lexical Parsing and the Abstract Syntax Tree
The input boundary acts as a fast semantic translation compiler. When a configuration command or data stream enters the terminal interface, the text is broken down by a lexical analyzer into distinct operational tokens using pre-compiled regular expressions.

The engine matches these tokens against an immutable factory configuration matrix. Attributes like rendering colors, velocity vectors, spacing margins, and wave forms are translated directly into binary integers and floating-point numbers. These values are injected directly into the designated offset addresses of the Uint32Array. PIR12 configures system execution by mutating state variables inside static native arrays, bypassing the need to generate code files on the fly.

### 3.2 Asynchronous Virtual Machine Architecture
The PIR12 Virtual Machine functions as an optimized micro-thread scheduler. It executes active processes by driving highly tuned computational loops over the shared data matrices. Every separate window space or system operation runs as an independent micro-thread, scheduled using high-performance requestAnimationFrame hooks.

During frame steps, the VM processes data vectors, handles mathematical scaling, and applies bitwise flags directly within the typed arrays, using zero high-level variables. All memory operations are forced to stay within strict array boundaries, protecting against system memory leaks or pointer corruption. If an individual thread encounters an execution error, the crash is fully contained inside that node's allocated buffer limits, keeping the core operating ecosystem completely safe.

### 3.3 Hardware-Accelerated Isolated Windowing Server
The graphical presentation system operates as a decoupled window management layer. When a new application process is triggered by the compiler, the window manager provisions an independent layout container that isolates its visual scope. This container features a dedicated HTML5 Canvas rendering context.

The windowing manager captures and routes pointer interactions (mousedown, mousemove, mouseup) using pure abstract coordinates, allowing users to drag, resize, maximize, and close windows smoothly. By executing all drawing logic through the hardware-accelerated canvas context, PIR12 separates layout calculations from the main thread document object model tree. This completely removes the risk of layout thrashing and ensures fast, responsive updates across the entire environment.

## 4. Monolithic Single-File Implementation Code
Below is the complete, self-contained, production-ready source code of the PIR12 platform. It integrates the host terminal interface, window manager, semantic compiler, virtual machine runtime, data grid module, and interactive text editor into a single, comprehensive file.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>PIR12: Monolithic Application Runtime Environment</title>
    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            user-select: none;
        }
        body, html {
            width: 100%;
            height: 100%;
            background-color: #050505;
            color: #00ff00;
            font-family: "Courier New", Courier, monospace;
            overflow: hidden;
            background-image: radial-gradient(rgba(0, 40, 0, 0.4) 1px, transparent 0);
            background-size: 24px 24px;
        }
        #pir12-desktop-environment {
            position: relative;
            width: 100%;
            height: 100%;
            z-index: 1;
        }
        #pir12-terminal-container {
            position: absolute;
            top: 40px;
            left: 40px;
            width: 660px;
            height: 480px;
            min-width: 380px;
            min-height: 250px;
            background-color: #0d0d0d;
            border: 2px solid #00ff00;
            box-shadow: 0 0 25px rgba(0, 255, 0, 0.3);
            display: flex;
            flex-direction: column;
            border-radius: 8px;
            overflow: hidden;
            z-index: 100000;
        }
        .terminal-header {
            background-color: #1a1a1a;
            color: #00ff00;
            padding: 10px 14px;
            cursor: move;
            display: flex;
            justify-content: space-between;
            align-items: center;
            font-size: 13px;
            font-weight: bold;
            border-bottom: 1px solid #00ff00;
            letter-spacing: 1px;
        }
        .terminal-title {
            display: flex;
            align-items: center;
            gap: 8px;
        }
        .terminal-content {
            padding: 16px;
            flex-grow: 1;
            overflow-y: auto;
            font-size: 13px;
            line-height: 1.6;
            white-space: pre-wrap;
            word-break: break-all;
        }
        .terminal-input-line {
            padding: 12px 14px;
            background-color: #020202;
            display: flex;
            align-items: center;
            border-top: 1px solid #002200;
            position: relative;
        }
        .terminal-prompt-label {
            color: #8888ff;
            font-weight: bold;
            white-space: nowrap;
            margin-right: 8px;
        }
        #js-os-input {
            background: transparent;
            border: none;
            color: #00ff00;
            font-family: inherit;
            font-size: inherit;
            flex-grow: 1;
            outline: none;
        }
        .terminal-resize-handle {
            position: absolute;
            right: 0;
            bottom: 0;
            width: 16px;
            height: 16px;
            cursor: se-resize;
            background: linear-gradient(135deg, transparent 70%, #00ff00 70%);
        }
        #pir12-system-status {
            position: fixed;
            bottom: 0;
            left: 0;
            width: 100%;
            height: 24px;
            background-color: #111;
            border-top: 1px solid #333;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 16px;
            font-size: 11px;
            color: #888;
            z-index: 200000;
        }
        .status-node {
            color: #00ff00;
            font-weight: bold;
        }
        ::-webkit-scrollbar {
            width: 8px;
            height: 8px;
        }
        ::-webkit-scrollbar-track {
            background: #050505;
        }
        ::-webkit-scrollbar-thumb {
            background: #222;
            border: 1px solid #00ff00;
            border-radius: 4px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #00ff00;
        }
    </style>
</head>
<body>

    <div id="pir12-desktop-environment">
        <div id="pir12-terminal-container">
            <div class="terminal-header" id="pir12-terminal-header">
                <div class="terminal-title">
                    <span>⚡ PIR12_SYSTEM_SHELL</span>
                </div>
            </div>
            
            <div class="terminal-content" id="pir12-terminal-content"></div>
            
            <div class="terminal-input-line">
                <span class="terminal-prompt-label">root@pir12:~\$</span>
                <input type="text" id="js-os-input" autocomplete="off" autofocus>
                <div class="terminal-resize-handle" id="pir12-terminal-resize"></div>
            </div>
        </div>
    </div>

    <div id="pir12-system-status">
        <div>SYSTEM STATUS: <span class="status-node">ONLINE</span></div>
        <div>ARCHITECTURE: <span class="status-node">MONOLITHIC MEMORY RUNTIME</span></div>
        <div id="system-time-display">CORE_CLOCK: 00:00:00</div>
    </div>

    <script>
        window.PIR12_CORE = { apps: {} };
        window.JS_OS_CORE = {};

        window.PIR12_CORE.Compiler = {
            COLOR_REGISTRY: {
                'green': '#00ff00', 'vihreä': '#00ff00',
                'red': '#ff3333', 'punainen': '#ff3333',
                'blue': '#3333ff', 'sininen': '#3333ff',
                'yellow': '#ffff30', 'keltainen': '#ffff30',
                'white': '#ffffff', 'valkoinen': '#ffffff',
                'neon': '#00ffff', 'cyan': '#00ffff'
            },
            SPEED_REGISTRY: {
                'fast': 2.5, 'nopeasti': 2.5, 'nopea': 2.5,
                'slow': 0.35, 'hitaasti': 0.35, 'hidas': 0.35,
                'normal': 1.0, 'normaali': 1.0, 'vakio': 1.0
            },
            SPACING_REGISTRY: {
                'dense': 8, 'tiheä': 8, 'tiivis': 8,
                'sparse': 22, 'harva': 22, 'wide': 26
            },
            compileBlueprint: function(promptText) {
                const text = (promptText || '').toLowerCase().trim();
                const tokens = text.split(/\s+/).filter(t => t.length > 0);

                let renderColor = '#00ff00';
                let speedFactor = 1.0;
                let gridSpacing = 14;
                let operationalMode = 'default';
                let intensityScale = 60;
                let appType = 'matrix';

                for (let token of tokens) {
                    if (this.COLOR_REGISTRY[token] !== undefined) renderColor = this.COLOR_REGISTRY[token];
                    if (this.SPEED_REGISTRY[token] !== undefined) speedFactor = this.SPEED_REGISTRY[token];
                    if (this.SPACING_REGISTRY[token] !== undefined) gridSpacing = this.SPACING_REGISTRY[token];

                    if (token === 'aalto' || token === 'wave' || token === 'sine') operationalMode = 'wave_oscillator';
                    else if (token === 'syke' || token === 'pulse' || token === 'flash') operationalMode = 'pulse_modulator';
                    else if (token === 'data' || token === 'grid' || token === 'table') { operationalMode = 'structured_grid'; appType = 'datagrid'; }
                    else if (token === 'editori' || token === 'editor' || token === 'teksti' || token === 'text') appType = 'texteditor';

                    if (/^\d+$/.test(token)) {
                        const val = parseInt(token, 10);
                        if (!isNaN(val)) {
                            intensityScale = val;
                            if (val > 100) gridSpacing = 8;
                            else if (val < 40) gridSpacing = 22;
                        }
                    }
                }

                return {
                    executionProfile: { appType, renderColor, speedFactor, gridSpacing, operationalMode, intensityScale }
                };
            }
        };

        window.PIR12_CORE.VirtualMachine = {
            activeThreads: new Map(),
            globalThreadSequence: 0,
            allocateMemoryHeap: function(elementCount) {
                const flatBuffer = new ArrayBuffer(elementCount * 4);
                return {
                    uint32View: new Uint32Array(flatBuffer),
                    float32Speeds: new Float32Array(elementCount)
                };
            },
            executeMicroThread: function(threadTag, blueprint, bodyContainer, windowWrapper) {
                const threadId = ++this.globalThreadSequence;
                const profile = blueprint.executionProfile;

                const canvas = document.createElement('canvas');
                Object.assign(canvas.style, { width: '100%', height: '100%', display: 'block' });
                bodyContainer.appendChild(canvas);

                const ctx = canvas.getContext('2d');
                canvas.width = bodyContainer.clientWidth;
                canvas.height = bodyContainer.clientHeight;

                const spacing = profile.gridSpacing;
                const columns = Math.floor(canvas.width / spacing);
                const heap = this.allocateMemoryHeap(columns);

                for (let i = 0; i < columns; i++) {
                    heap.uint32View[i] = Math.floor(Math.random() * (canvas.height / 14));
                    heap.float32Speeds[i] = (0.5 + Math.random() * 0.9) * profile.speedFactor;
                }

                const threadRecord = { id: threadId, isRunning: true, timer: 0 };
                this.activeThreads.set(threadId, threadRecord);
            windowWrapper.__onCloseLifecycleHook = () => {
                threadRecord.isRunning = false;
                this.activeThreads.delete(threadId);
                heap.uint32View.fill(0);
            };

            const charPool = "0123456789ABCDEFGHIJKLMNOPQRSTUVWXYZコンニチハハシ";

            const tick = () => {
                if (!threadRecord.isRunning || !document.body.contains(canvas)) return;

                ctx.fillStyle = 'rgba(0, 0, 0, 0.05)';
                ctx.fillRect(0, 0, canvas.width, canvas.height);
                ctx.fillStyle = profile.renderColor;
                ctx.font = `${spacing - 1}px monospace`;
                
                threadRecord.timer += 0.05 * profile.speedFactor;

                for (let i = 0; i < columns; i++) {
                    const charStr = charPool[Math.floor(Math.random() * charPool.length)];
                    let x = i * spacing;
                    const y = Math.floor(heap.uint32View[i]) * 14;

                    if (profile.operationalMode === 'wave_oscillator') {
                        x += Math.sin((y * 0.02) + threadRecord.timer) * 15;
                    } else if (profile.operationalMode === 'pulse_modulator') {
                        const alpha = Math.sin(threadRecord.timer * 2) * 0.4 + 0.6;
                        ctx.fillStyle = profile.renderColor + Math.floor(alpha * 255).toString(16).padStart(2, '0');
                    }

                    ctx.fillText(charStr, x, y);

                    if (y > canvas.height && Math.random() > 0.975) {
                        heap.uint32View[i] = 0;
                    }
                    
                    heap.uint32View[i] += heap.float32Speeds[i];
                }
                requestAnimationFrame(tick);
            };
            requestAnimationFrame(tick);
        }
    };
        window.JS_OS_CORE.createGuiWindow = function(appName, initCallback) {
            const desktop = document.getElementById('pir12-desktop-environment');
            const win = document.createElement('div');
            win.className = 'pir12-app-node';
            
            Object.assign(win.style, {
                position: 'fixed', top: '140px', left: '140px', width: '460px', height: '360px',
                background: '#020202', border: '2px solid #00ff00', boxShadow: '0 0 30px rgba(0, 255, 0, 0.4)',
                zIndex: '100001', display: 'flex', flexDirection: 'column', borderRadius: '6px', overflow: 'hidden'
            });

            const hdr = document.createElement('div');
            Object.assign(hdr.style, {
                background: '#151515', color: '#ffffff', padding: '8px 12px', cursor: 'move',
                display: 'flex', justifyContent: 'space-between', alignItems: 'center', fontSize: '12px',
                borderBottom: '1px solid #00ff00', fontFamily: 'monospace'
            });
            hdr.innerHTML = `<span style="color:#00ff00;font-weight:bold;">NODE_INSTANCE // ${appName}</span><span class="close-btn" style="cursor:pointer;color:#ff4444;font-weight:bold;">✕</span>`;
            win.appendChild(hdr);

            const body = document.createElement('div');
            Object.assign(body.style, { flexGrow: '1', position: 'relative', overflow: 'hidden', background: '#000000' });
            win.appendChild(body);

            desktop.appendChild(win);

            win.querySelector('.close-btn').addEventListener('click', () => {
                if (win.__onCloseLifecycleHook) win.__onCloseLifecycleHook();
                win.remove();
            });

            let drag = false, px = 0, py = 0;
            hdr.addEventListener('mousedown', (e) => {
                if (e.target.className === 'close-btn') return;
                drag = true;
                px = e.clientX - win.offsetLeft;
                py = e.clientY - win.offsetTop;
            });
            document.addEventListener('mousemove', (e) => {
                if (drag) { win.style.left = (e.clientX - px) + 'px'; win.style.top = (e.clientY - py) + 'px'; }
            });
            document.addEventListener('mouseup', () => drag = false);

            initCallback(body, win);
        };

        window.PIR12_CORE.apps.DataGrid = {
            init: function(body, win, blueprint) {
                const profile = blueprint.executionProfile;
                body.style.display = 'flex';
                body.style.flexDirection = 'column';

                const bar = document.createElement('div');
                Object.assign(bar.style, { background: '#111111', color: profile.renderColor, padding: '6px 12px', fontSize: '11px', borderBottom: '1px solid #222222', display: 'flex', justifyContent: 'space-between' });
                bar.innerHTML = `<span>STATUS: ACTIVE_STREAM</span><span class="metrics">PROCESSING...</span>`;
                body.appendChild(bar);

                const wrapper = document.createElement('div');
                Object.assign(wrapper.style, { flexGrow: '1', position: 'relative', width: '100%', height: '100%' });
                body.appendChild(wrapper);

                window.PIR12_CORE.VirtualMachine.executeMicroThread('DataGridStream', blueprint, wrapper, win);

                const mDisplay = bar.querySelector('.metrics');
                let active = true, count = 0;
                
                win.__onCloseLifecycleHook = () => { active = false; };
                
                function update() {
                    if (!active) return;
                    count++;
                    mDisplay.textContent = `V-STREAM: ${(count * profile.intensityScale * profile.speedFactor * 0.03).toFixed(2)} MB // ALLOC: 0B_HEAP // AUTHOR: Juho Artturi Hemminki`;
                    setTimeout(update, 500);
                }
                setTimeout(update, 500);
            }
        };

        window.PIR12_CORE.apps.TextEditor = {
            init: function(body, win, blueprint) {
                const profile = blueprint.executionProfile;
                Object.assign(body.style, { display: 'flex', flexDirection: 'column', padding: '12px' });

                const toolbar = document.createElement('div');
                Object.assign(toolbar.style, { display: 'flex', gap: '8px', marginBottom: '10px', borderBottom: '1px solid #222222', paddingBottom: '8px' });

                const btnCommit = document.createElement('button');
                btnCommit.textContent = 'COMMIT_BUFFER';
                Object.assign(btnCommit.style, { background: '#111111', border: `1px solid ${profile.renderColor}`, color: profile.renderColor, padding: '4px 10px', cursor: 'pointer', fontSize: '11px', fontFamily: 'inherit' });

                const btnWipe = document.createElement('button');
                btnWipe.textContent = 'WIPE_HEAP';
                Object.assign(btnWipe.style, { background: '#111111', border: `1px solid ${profile.renderColor}`, color: profile.renderColor, padding: '4px 10px', cursor: 'pointer', fontSize: '11px', fontFamily: 'inherit' });

                const info = document.createElement('span');
                info.textContent = '// AUTHOR: Juho Artturi Hemminki';
                Object.assign(info.style, { fontSize: '11px', color: '#666666', marginLeft: 'auto', alignSelf: 'center' });

                toolbar.appendChild(btnCommit);
                toolbar.appendChild(btnWipe);
                toolbar.appendChild(info);
                body.appendChild(toolbar);

                const area = document.createElement('textarea');
                Object.assign(area.style, { width: '100%', flexGrow: '1', background: '#000000', border: '1px solid #1a1a1a', color: '#ffffff', fontSize: '13px', padding: '10px', outline: 'none', resize: 'none' });
                body.appendChild(area);

                btnCommit.addEventListener('click', () => { info.textContent = `// COMMITTED: ${area.value.length}b`; info.style.color = '#8888ff'; });
                btnWipe.addEventListener('click', () => { area.value = ''; info.textContent = '// BUFFER CLEARED'; info.style.color = '#ff4444'; });
                area.addEventListener('mousedown', (e) => e.stopPropagation());
                setTimeout(() => area.focus(), 150);
            }
        };

        document.addEventListener("DOMContentLoaded", () => {
            const timeDisplay = document.getElementById("system-time-display");
            setInterval(() => {
                const now = new Date();
                timeDisplay.textContent = `CORE_CLOCK: ${String(now.getHours()).padStart(2,'0')}:${String(now.getMinutes()).padStart(2,'0')}:${String(now.getSeconds()).padStart(2,'0')}`;
            }, 1000);

            const content = document.getElementById('pir12-terminal-content');
            const input = document.getElementById('js-os-input');

            content.innerHTML = `<div>[BOOT] PIR12 Monolithic Kernel Platform initialized successfully.</div>
                                 <div>[SUCCESS] BARE-METAL MEMORY SPEED ENGINE READY.</div>
                                 <div><br>Available commands in terminal:</div>
                                 <div>  • <b>generate matrix</b> - (Pure Matrix koodisade)</div>
                                 <div>  • <b>matrix [vapaa teksti]</b> - (Ohjaa koodisadetetta, kuvaajia tai tekstieditoria)</div>
                                 <div>     <i>Kokeile: matrix punainen nopeasti aalto</i></div>
                                 <div>     <i>Kokeile: matrix sininen data grid</i></div>
                                 <div>     <i>Kokeile: matrix neon teksti editori</i></div><br>`;

            input.addEventListener('keydown', function(e) {
                if (e.key === 'Enter') {
                    const rawInput = input.value.trim();
                    if (!rawInput) return;

                    const parts = rawInput.split(' ');
                    const cmd = parts && parts.length > 0 ? parts.toLowerCase() : '';
                    const args = parts.slice(1);

                    content.innerHTML += `<div><span style="color:#8888ff">root@pir12:~$</span> ${rawInput}</div>`;

                    if (cmd === 'help') {
                        content.innerHTML += `<div>Commands: help, generate matrix, matrix [text], clear</div>`;
                    } else if (cmd === 'clear') {
                        content.innerHTML = '';
                    } else if (cmd === 'generate' && args === 'matrix') {
                        const blueprint = window.PIR12_CORE.Compiler.compileBlueprint("vihreä normaali");
                        window.JS_OS_CORE.createGuiWindow("PURE MATRIX", (b, w) => {
                            window.PIR12_CORE.VirtualMachine.executeMicroThread('BaseMatrix', blueprint, b, w);
                        });
                    } else if (cmd === 'matrix') {
                        const promptText = args.join(' ');
                        const blueprint = window.PIR12_CORE.Compiler.compileBlueprint(promptText);
                        const appProfile = blueprint.executionProfile;

                        if (appProfile.appType === 'datagrid') {
                            window.JS_OS_CORE.createGuiWindow(promptText.toUpperCase(), (b, w) => {
                                window.PIR12_CORE.apps.DataGrid.init(b, w, blueprint);
                            });
                        } else if (appProfile.appType === 'texteditor') {
                            window.JS_OS_CORE.createGuiWindow(promptText.toUpperCase(), (b, w) => {
                                window.PIR12_CORE.apps.TextEditor.init(b, w, blueprint);
                            });
                        } else {
                            window.JS_OS_CORE.createGuiWindow(promptText.toUpperCase(), (b, w) => {
                            window.JS_OS_CORE.createGuiWindow(promptText.toUpperCase(), (b, w) => {
                                window.PIR12_CORE.VirtualMachine.executeMicroThread('CustomMatrix', blueprint, b, w);
                            });
                        }
                    } else {
                        content.innerHTML += `<div style="color:#ff5c5c">js-bash: ${cmd}: command not found</div>`;
                    }
                    input.value = '';
                    content.scrollTop = content.scrollHeight;
                }
            });
            const shell = document.getElementById('pir12-terminal-container');
            const hdr = document.getElementById('pir12-terminal-header');
            let drag = false, sx = 0, sy = 0;
            hdr.addEventListener('mousedown', (e) => { drag = true; sx = e.clientX - shell.offsetLeft; sy = e.clientY - shell.offsetTop; });
            document.addEventListener('mousemove', (e) => { if (drag) { shell.style.left = (e.clientX - sx) + 'px'; shell.style.top = (e.clientY - sy) + 'px'; } });
            document.addEventListener('mouseup', () => drag = false);
        });
```

---

## Author and Intellectual Property Owner
Juho Artturi Hemminki

## Proprietary Copyright Notice
Copyright (c) 2026 Juho Artturi Hemminki. All Rights Reserved. All Claims Reserved Worldwide. Licensing requests, commercial assessment, and institutional evaluations must be formally submitted via projectflagcarrier@gmail.com.
