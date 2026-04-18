```react
import React, { useState, useEffect, useRef } from 'react';
import { 
  Play, Pause, SkipForward, SkipBack, Volume2, Monitor, 
  Search, Globe, ArrowLeft, ArrowRight, RotateCcw, Home, 
  X, Square, Minus, Download, Layout, Activity, AlertTriangle, 
  Bug, ExternalLink, HardDrive, Music, Video, PlusSquare, ShieldAlert,
  Cpu, Settings, RefreshCw
} from 'lucide-react';

const App = () => {
  const [activeApp, setActiveApp] = useState('DESKTOP'); 
  const [bsodData, setBsodData] = useState(null);
  const [arch, setArch] = useState('64-bit');
  const [isRebooting, setIsRebooting] = useState(false);
  
  const openApp = (app) => setActiveApp(app);

  const triggerReboot = () => {
    setActiveApp('DESKTOP');
    setIsRebooting(true);
    setTimeout(() => {
      setIsRebooting(false);
    }, 3000);
  };

  return (
    <div className="h-screen w-full bg-[#1e1e1e] flex items-center justify-center font-sans select-none overflow-hidden">
      {/* The "Small Desktop" Container */}
      <div className="w-[1024px] h-[768px] bg-[#3a6ea5] relative shadow-2xl border-4 border-[#333] overflow-hidden flex flex-col scale-[0.85] md:scale-100 origin-center">
        
        {/* Reboot Overlay (Contained within desktop) */}
        {isRebooting && <RebootSequence arch={arch} />}

        {/* BSOD Layer */}
        {!isRebooting && activeApp === 'BSOD' && (
          <BSODScreen 
            error={bsodData} 
            arch={arch} 
            onReset={triggerReboot} 
          />
        )}

        {/* Desktop Workspace */}
        <div className="flex-1 relative p-4 grid grid-cols-1 grid-rows-10 gap-2 w-20">
          <DesktopIcon icon={<Music size={32} />} label="Media" onClick={() => openApp('WMP')} />
          <DesktopIcon icon={<Globe size={32} />} label="Browser" onClick={() => openApp('IE')} />
          <DesktopIcon icon={<Download size={32} />} label="Apps" onClick={() => openApp('STORE')} />
          <DesktopIcon icon={<Activity size={32} />} label="Tasks" onClick={() => openApp('TASKMGR')} />
        </div>

        {/* Small App Windows */}
        <div className="absolute inset-0 pointer-events-none flex items-center justify-center">
          <div className="pointer-events-auto relative w-full h-full">
            {activeApp === 'WMP' && <WindowsMediaPlayer onClose={() => setActiveApp('DESKTOP')} />}
            {activeApp === 'IE' && <InternetExplorer onClose={() => setActiveApp('DESKTOP')} />}
            {activeApp === 'STORE' && <AppStore onClose={() => setActiveApp('DESKTOP')} />}
            {activeApp === 'TASKMGR' && (
              <TaskManager 
                arch={arch}
                setArch={setArch}
                onClose={() => setActiveApp('DESKTOP')} 
                onReboot={triggerReboot}
                onCrash={(data) => {
                  setBsodData(data);
                  setActiveApp('BSOD');
                }} 
              />
            )}
          </div>
        </div>

        {/* Taskbar */}
        <div className="h-10 bg-[#c0c7d8] border-t border-white flex items-center px-1 z-50">
          <button 
            className="flex items-center gap-1 bg-[#225ad7] text-white px-3 py-1 italic font-bold rounded-tr-xl rounded-br-xl shadow-inner border-r-2 border-b-2 border-black/20"
            onClick={() => setActiveApp('DESKTOP')}
          >
            <Monitor size={16} /> start
          </button>
          <div className="flex-1 flex gap-1 px-2">
             {activeApp !== 'DESKTOP' && activeApp !== 'BSOD' && (
               <div className="bg-white/40 border-t border-l border-white border-b border-r border-gray-600 px-4 py-1 text-xs font-medium">
                 {activeApp}
               </div>
             )}
          </div>
          <div className="bg-[#107ce3] text-white px-4 py-1 text-xs flex items-center border-l border-[#085bb0]">
            {new Date().toLocaleTimeString([], { hour: '2-digit', minute: '2-digit' })}
          </div>
        </div>
      </div>
    </div>
  );
};

// --- REBOOT SEQUENCE COMPONENT ---
const RebootSequence = ({ arch }) => {
  return (
    <div className="absolute inset-0 bg-black text-gray-300 font-mono p-8 text-sm flex flex-col gap-1 z-[10000]">
      <p>KanuOS BIOS v4.0.29</p>
      <p>Copyright (C) 2024 Kanu Technologies Inc.</p>
      <p className="mt-4">CPU: Kanu-Core {arch} Processor</p>
      <p>Memory Test: 16384KB OK</p>
      <p className="mt-4">Detecting primary master... [OK]</p>
      <p>Detecting secondary master... [OK]</p>
      <p className="mt-4 text-white animate-pulse">Loading Kernel Core...</p>
      <div className="mt-auto flex justify-between opacity-50">
        <span>Press DEL to enter Setup</span>
        <span>04/18/2026-KCore-{arch}</span>
      </div>
    </div>
  );
};

const DesktopIcon = ({ icon, label, onClick }) => (
  <div 
    className="flex flex-col items-center gap-1 cursor-pointer hover:bg-white/20 p-2 rounded transition-colors group"
    onClick={onClick}
  >
    <div className="text-white drop-shadow-md group-active:scale-95">{icon}</div>
    <span className="text-white text-[9px] text-center font-medium drop-shadow-md">{label}</span>
  </div>
);

// --- WINDOWS MEDIA PLAYER ---
const WindowsMediaPlayer = ({ onClose }) => {
  const [isPlaying, setIsPlaying] = useState(false);
  return (
    <div className="absolute top-20 left-20 w-[500px] h-[350px] bg-[#1a1a1c] border border-gray-600 shadow-xl flex flex-col text-white rounded-lg overflow-hidden">
      <div className="h-7 bg-gradient-to-r from-[#003366] to-[#0078d7] flex items-center justify-between px-2">
        <div className="flex items-center gap-2 text-[10px] font-semibold"><Music size={12} /> Media Player</div>
        <button className="hover:bg-red-500 p-1" onClick={onClose}><X size={12} /></button>
      </div>
      <div className="flex-1 bg-black flex flex-col items-center justify-center">
         <div className="flex items-end gap-1 h-20 mb-4">
            {[...Array(10)].map((_, i) => (
                <div key={i} className="w-3 bg-blue-500 opacity-60 rounded-t" style={{ height: isPlaying ? `${Math.random() * 100}%` : '10%', transition: 'height 0.2s' }} />
            ))}
         </div>
         <p className="text-xs text-gray-400">Audio Loop 0.25s Active</p>
      </div>
      <div className="h-14 bg-[#2d2d30] border-t border-white/10 flex items-center justify-center gap-4">
        <SkipBack size={16} />
        <button onClick={() => setIsPlaying(!isPlaying)} className="w-8 h-8 rounded-full bg-blue-600 flex items-center justify-center">{isPlaying ? <Pause size={16} /> : <Play size={16} />}</button>
        <SkipForward size={16} />
      </div>
    </div>
  );
};

// --- INTERNET EXPLORER ---
const InternetExplorer = ({ onClose }) => (
  <div className="absolute top-10 left-40 w-[600px] h-[400px] bg-[#f0f0f0] border-2 border-[#0054e3] shadow-xl flex flex-col text-black rounded-sm overflow-hidden border-t-0">
    <div className="h-7 bg-[#0054e3] flex items-center justify-between px-2 text-white">
      <div className="flex items-center gap-2 text-[10px] font-bold"><Globe size={12} /> Explorer</div>
      <button className="bg-[#cc0000] px-3 h-full" onClick={onClose}><X size={12} /></button>
    </div>
    <div className="bg-[#efefde] border-b border-gray-400 p-1 flex items-center gap-2">
      <div className="flex-1 bg-white border border-gray-400 h-5 px-2 text-[10px]">http://www.kanu-os.net</div>
    </div>
    <div className="flex-1 bg-white flex flex-col items-center justify-center p-4">
        <h1 className="text-2xl font-bold text-blue-800">KanuOS Web</h1>
        <p className="text-[10px] text-gray-500">Welcome to the small desktop browser.</p>
    </div>
  </div>
);

// --- APP STORE ---
const AppStore = ({ onClose }) => (
  <div className="absolute top-40 left-32 w-[450px] h-[300px] bg-white border border-gray-400 shadow-xl flex flex-col text-black rounded-lg overflow-hidden">
    <div className="h-10 bg-white border-b border-gray-200 flex items-center justify-between px-4">
      <div className="flex items-center gap-2 font-bold text-xs">🛍️ App Store</div>
      <button onClick={onClose} className="hover:bg-gray-100 p-1 rounded-full"><X size={16} /></button>
    </div>
    <div className="flex-1 p-4 grid grid-cols-2 gap-2 overflow-y-auto bg-gray-50">
      {[1, 2, 3, 4].map(i => (
        <div key={i} className="bg-white p-2 border border-gray-200 rounded text-[10px] flex flex-col gap-1">
          <div className="font-bold">Software #{i}</div>
          <button className="bg-blue-100 text-blue-700 rounded py-1">Install</button>
        </div>
      ))}
    </div>
  </div>
);

// --- TASK MANAGER ---
const TaskManager = ({ onClose, onCrash, onReboot, arch, setArch }) => {
  const [tab, setTab] = useState('processes');
  return (
    <div className="absolute top-10 left-10 w-[420px] h-[500px] bg-[#f0f0f0] border-2 border-gray-300 shadow-2xl flex flex-col text-black text-[10px]">
      <div className="h-7 bg-white flex items-center justify-between px-2 border-b border-gray-400 font-bold">
        <span className="flex items-center gap-1"><Activity size={12} /> Task Manager</span>
        <button onClick={onClose}><X size={12} /></button>
      </div>
      <div className="flex bg-[#f0f0f0] p-1 border-b border-gray-300 gap-2">
        {['Processes', 'Performance', 'Architecture', 'NotMyFault'].map(t => (
          <button key={t} onClick={() => setTab(t.toLowerCase())} className={`px-2 py-0.5 border border-gray-400 ${tab === t.toLowerCase() ? 'bg-white' : ''}`}>{t}</button>
        ))}
      </div>
      <div className="flex-1 bg-white border border-gray-400 m-2 p-2 overflow-auto">
        {tab === 'processes' && <div>System running at {arch}...</div>}
        {tab === 'architecture' && (
          <div className="space-y-4">
            <h3 className="font-bold border-b pb-1">Processor Bits</h3>
            <div className="flex flex-col gap-2">
              <label className="flex items-center gap-2"><input type="radio" checked={arch === '32-bit'} onChange={() => setArch('32-bit')} /> 32-bit Core</label>
              <label className="flex items-center gap-2"><input type="radio" checked={arch === '64-bit'} onChange={() => setArch('64-bit')} /> 64-bit Core</label>
            </div>
          </div>
        )}
        {tab === 'notmyfault' && (
          <div className="flex flex-col gap-2">
            <p className="text-red-600 font-bold italic">Simulate System Event:</p>
            <button onClick={() => onCrash({ code: 'CRITICAL_PROCESS_DIED', stop: '0x000000EF' })} className="border p-2 bg-gray-50 hover:bg-red-50 text-left flex items-center gap-2"><Bug size={14} /> Force Kernel BSOD</button>
            <button onClick={onReboot} className="border p-2 bg-gray-50 hover:bg-blue-50 text-left flex items-center gap-2"><RefreshCw size={14} /> Restart System (No BSOD)</button>
          </div>
        )}
      </div>
      <div className="p-2 border-t border-gray-300 flex justify-between">
        <span>Bits: {arch}</span>
        <span>CPU: 2%</span>
      </div>
    </div>
  );
};

// --- BSOD SCREEN ---
const BSODScreen = ({ error, onReset, arch }) => {
  const [percent, setPercent] = useState(0);

  useEffect(() => {
    let audioCtx;
    let oscillator;
    let gainNode;

    const startStuckAudio = () => {
      try {
        audioCtx = new (window.AudioContext || window.webkitAudioContext)();
        oscillator = audioCtx.createOscillator();
        gainNode = audioCtx.createGain();
        oscillator.type = 'sawtooth';
        oscillator.frequency.setValueAtTime(55, audioCtx.currentTime); 

        const stutterRate = 0.25; 
        const now = audioCtx.currentTime;
        for (let i = 0; i < 200; i++) {
            const time = now + (i * stutterRate);
            oscillator.frequency.setTargetAtTime(100, time, 0.01);
            oscillator.frequency.setTargetAtTime(55, time + 0.1, 0.01);
        }

        gainNode.gain.setValueAtTime(0.08, audioCtx.currentTime); 
        oscillator.connect(gainNode);
        gainNode.connect(audioCtx.destination);
        oscillator.start();
      } catch (e) {}
    };

    startStuckAudio();
    const interval = setInterval(() => {
      setPercent(p => (p >= 100 ? 100 : p + 15));
    }, 1200);

    return () => {
      clearInterval(interval);
      if (oscillator) oscillator.stop();
      if (audioCtx) audioCtx.close();
    };
  }, []);

  return (
    <div className="absolute inset-0 bg-[#0078d7] text-white p-8 flex flex-col font-sans z-[100]">
      <div className="text-[64px] mb-4">:(</div>
      <div className="text-lg leading-tight mb-4 max-w-lg">
        Your small desktop ran into a problem and needs to restart. We're just collecting some error info.
      </div>
      <div className="text-lg mb-8">{Math.min(percent, 100)}% complete</div>
      
      <div className="flex gap-4 items-start">
        <div className="w-20 h-20 bg-white p-1 shrink-0">
          <div className="w-full h-full bg-black flex flex-wrap">
             {[...Array(16)].map((_, i) => (
               <div key={i} className={`w-1/4 h-1/4 ${Math.random() > 0.5 ? 'bg-white' : 'bg-black'}`} />
             ))}
          </div>
        </div>
        <div className="text-[10px] opacity-80 space-y-2">
          <p>Stop code: {error?.code}</p>
          <p>Arch: {arch}</p>
          <p>Fault: {arch === '32-bit' ? 'WOW64_STUTTER' : 'AMD64_HARD_FREEZE'}</p>
          <p className="italic text-[8px] mt-2">Audio loop active at 0.25s interval.</p>
        </div>
      </div>

      {percent >= 100 && (
        <button onClick={onReset} className="mt-auto text-blue-200 underline text-xs text-left">Click here to reboot the bits.</button>
      )}
    </div>
  );
};

export default App;

```
           
