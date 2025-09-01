<svg width="1200" height="400" viewBox="0 0 1200 400" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <!-- Gradiente rosso -->
    <linearGradient id="redGradient" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:#ff0000;stop-opacity:1" />
      <stop offset="50%" style="stop-color:#cc0000;stop-opacity:0.8" />
      <stop offset="100%" style="stop-color:#990000;stop-opacity:0.6" />
    </linearGradient>
    
    <!-- Filtro glow -->
    <filter id="glow">
      <feGaussianBlur stdDeviation="3" result="coloredBlur"/>
      <feMerge> 
        <feMergeNode in="coloredBlur"/>
        <feMergeNode in="SourceGraphic"/>
      </feMerge>
    </filter>
  </defs>
  
  <!-- Sfondo nero -->
  <rect width="1200" height="400" fill="#000000"/>
  
  <!-- Onde animate -->
  <g filter="url(#glow)">
    <!-- Onda 1 -->
    <path d="M0,200 Q150,100 300,200 T600,200 T900,200 T1200,200 L1200,400 L0,400 Z" 
          fill="none" stroke="#ff0000" stroke-width="2" opacity="0.8">
      <animateTransform attributeName="transform" type="translate" 
                        values="0,0; 100,0; 0,0" dur="8s" repeatCount="indefinite"/>
      <animate attributeName="d" dur="6s" repeatCount="indefinite"
               values="M0,200 Q150,100 300,200 T600,200 T900,200 T1200,200 L1200,400 L0,400 Z;
                       M0,180 Q150,120 300,180 T600,180 T900,180 T1200,180 L1200,400 L0,400 Z;
                       M0,200 Q150,100 300,200 T600,200 T900,200 T1200,200 L1200,400 L0,400 Z"/>
    </path>
    
    <!-- Onda 2 -->
    <path d="M0,150 Q200,80 400,150 T800,150 T1200,150" 
          fill="none" stroke="#ff3333" stroke-width="3" opacity="0.9">
      <animateTransform attributeName="transform" type="translate" 
                        values="0,0; -120,0; 0,0" dur="10s" repeatCount="indefinite"/>
      <animate attributeName="d" dur="7s" repeatCount="indefinite"
               values="M0,150 Q200,80 400,150 T800,150 T1200,150;
                       M0,170 Q200,60 400,170 T800,170 T1200,170;
                       M0,150 Q200,80 400,150 T800,150 T1200,150"/>
    </path>
    
    <!-- Onda 3 -->
    <path d="M0,250 Q100,180 200,250 Q300,320 400,250 Q500,180 600,250 Q700,320 800,250 Q900,180 1000,250 Q1100,320 1200,250" 
          fill="none" stroke="#ff6666" stroke-width="2" opacity="0.7">
      <animateTransform attributeName="transform" type="translate" 
                        values="0,0; 80,0; 0,0" dur="12s" repeatCount="indefinite"/>
    </path>
    
    <!-- Onda 4 - Contorno interno -->
    <path d="M0,120 Q250,60 500,120 T1000,120 T1200,120" 
          fill="none" stroke="#ff9999" stroke-width="1" opacity="0.6">
      <animateTransform attributeName="transform" type="translate" 
                        values="0,0; -60,0; 0,0" dur="15s" repeatCount="indefinite"/>
    </path>
    
    <!-- Onda 5 - Livello inferiore -->
    <path d="M0,300 Q150,240 300,300 Q450,360 600,300 Q750,240 900,300 Q1050,360 1200,300" 
          fill="none" stroke="#cc0000" stroke-width="2" opacity="0.8">
      <animateTransform attributeName="transform" type="translate" 
                        values="0,0; 90,0; 0,0" dur="9s" repeatCount="indefinite"/>
    </path>
    
    <!-- Cerchi concentrici animati -->
    <g>
      <circle cx="200" cy="150" r="30" fill="none" stroke="#ff0000" stroke-width="2" opacity="0.6">
        <animate attributeName="r" values="20;40;20" dur="4s" repeatCount="indefinite"/>
        <animate attributeName="opacity" values="0.8;0.3;0.8" dur="4s" repeatCount="indefinite"/>
      </circle>
      <circle cx="200" cy="150" r="20" fill="none" stroke="#ff3333" stroke-width="1" opacity="0.8">
        <animate attributeName="r" values="15;25;15" dur="4s" repeatCount="indefinite"/>
      </circle>
    </g>
    
    <g>
      <circle cx="800" cy="280" r="25" fill="none" stroke="#ff0000" stroke-width="2" opacity="0.5">
        <animate attributeName="r" values="15;35;15" dur="5s" repeatCount="indefinite"/>
        <animate attributeName="opacity" values="0.7;0.2;0.7" dur="5s" repeatCount="indefinite"/>
      </circle>
      <circle cx="800" cy="280" r="15" fill="none" stroke="#ff6666" stroke-width="1" opacity="0.7">
        <animate attributeName="r" values="10;20;10" dur="5s" repeatCount="indefinite"/>
      </circle>
    </g>
    
    <!-- Forme organiche animate -->
    <path d="M400,100 Q450,50 500,100 Q550,150 500,200 Q450,250 400,200 Q350,150 400,100 Z" 
          fill="none" stroke="#ff4444" stroke-width="2" opacity="0.7">
      <animateTransform attributeName="transform" type="rotate" 
                        values="0 450 150; 360 450 150" dur="20s" repeatCount="indefinite"/>
      <animate attributeName="opacity" values="0.7;0.3;0.7" dur="6s" repeatCount="indefinite"/>
    </path>
    
    <path d="M900,320 Q920,300 940,320 Q960,340 940,360 Q920,380 900,360 Q880,340 900,320 Z" 
          fill="none" stroke="#ff7777" stroke-width="1" opacity="0.6">
      <animateTransform attributeName="transform" type="rotate" 
                        values="0 920 340; -360 920 340" dur="18s" repeatCount="indefinite"/>
    </path>
  </g>
  
  <!-- Testo Rockroky centrato -->
  <text x="600" y="200" font-family="Arial, sans-serif" font-size="60" font-weight="bold" 
        text-anchor="middle" fill="#ffffff" filter="url(#glow)">
    Rockroky 👋
    <animate attributeName="opacity" values="0.8;1;0.8" dur="3s" repeatCount="indefinite"/>
  </text>
</svg>
