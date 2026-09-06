# ⌨️ Códigos Padrão

#### Spawn de Pacote (`spawn`)

```html
<!-- OVERLAY: SPAWN DE PACOTE -->
<style>
  @import url('https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@600;700&family=JetBrains+Mono:wght@700&display=swap');
  * { box-sizing: border-box; margin: 0; padding: 0; }
  body { background: transparent; overflow: hidden; font-family: 'Space Grotesk', sans-serif; }

  .spawn-container {
    position: fixed;
    top: 32px;
    right: 32px;
    display: flex;
    flex-direction: column;
    align-items: flex-end;
    animation: bounceIn 0.6s cubic-bezier(0.34, 1.56, 0.64, 1) forwards;
  }

  .tag-pill {
    display: flex;
    align-items: center;
    gap: 8px;
    background: #ffffff;
    color: #101828;
    font-family: 'JetBrains Mono', monospace;
    font-size: 11px;
    font-weight: 700;
    padding: 6px 14px;
    border-radius: 12px;
    border: 2px solid #101828;
    box-shadow: 3px 3px 0px #101828;
    margin-bottom: 12px;
    text-transform: uppercase;
  }

  .tag-dot {
    width: 10px;
    height: 10px;
    border-radius: 50%;
    background: #c8ff3d;
    border: 1px solid #101828;
    animation: pulse 1.5s infinite;
  }

  .card-box {
    background: #101828;
    border-radius: 24px;
    padding: 20px;
    border: 2px solid #2563ff;
    box-shadow: 6px 6px 0px #2563ff;
    width: 300px;
    display: flex;
    flex-direction: column;
    align-items: center;
    position: relative;
    overflow: hidden;
  }

  .pack-image {
    width: 180px;
    height: 180px;
    object-fit: contain;
    filter: drop-shadow(0 15px 25px rgba(0,0,0,0.7));
    margin: 8px 0;
  }

  .pack-title {
    color: #ffffff;
    font-size: 18px;
    font-weight: 700;
    text-align: center;
    max-width: 100%;
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
  }

  .cta-btn {
    margin-top: 14px;
    width: 100%;
    background: #c8ff3d;
    color: #101828;
    font-family: 'JetBrains Mono', monospace;
    font-size: 12px;
    font-weight: 700;
    padding: 10px 16px;
    border-radius: 12px;
    border: 2px solid #101828;
    text-align: center;
  }

  @keyframes bounceIn {
    0% { transform: scale(0.7) translateY(-30px); opacity: 0; }
    100% { transform: scale(1) translateY(0); opacity: 1; }
  }
  @keyframes pulse { 0%, 100% { opacity: 1; } 50% { opacity: 0.7; } }
</style>

<div class="spawn-container">
  <div class="tag-pill">
    <span class="tag-dot"></span>
    <span>✦ DROP DETECTADO NO CHAT</span>
  </div>

  <div class="card-box">
    <img id="pack-img" class="pack-image" src="{{data.image}}" alt="{{data.packName}}" />
    <h3 id="pack-name" class="pack-title">{{data.packName}}</h3>
    <div class="cta-btn">
      ⚡ DIGITE <span id="pack-trigger">{{data.triggers.claim}}</span>
    </div>
  </div>
</div>
```

***

#### 5.10. Duelo de Cartas (`duel`)

```html
<!-- OVERLAY: DUELO DE CARTAS -->
<style>
  @import url('https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@600;700&family=JetBrains+Mono:wght@700&display=swap');
  * { box-sizing: border-box; margin: 0; padding: 0; }
  body { background: transparent; overflow: hidden; font-family: 'Space Grotesk', sans-serif; }

  .duel-screen {
    width: 100vw;
    height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 32px;
  }

  .duel-card {
    background: rgba(16, 24, 40, 0.98);
    border-radius: 40px;
    padding: 36px 48px;
    border: 2px solid #ff714b;
    box-shadow: 8px 8px 0px #ff714b;
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  .duel-tag {
    background: #ff714b;
    color: #101828;
    font-family: 'JetBrains Mono', monospace;
    font-size: 11px;
    font-weight: 700;
    padding: 6px 16px;
    border-radius: 12px;
    border: 2px solid #101828;
    text-transform: uppercase;
    margin-bottom: 24px;
  }

  .vs-row {
    display: flex;
    align-items: center;
    gap: 32px;
  }

  .card-box {
    width: 150px;
    height: 210px;
    border-radius: 16px;
    background: #000;
    border: 2px solid #2563ff;
    overflow: hidden;
  }

  .card-box img { width: 100%; height: 100%; object-fit: contain; }

  .vs-badge {
    font-size: 28px;
    font-weight: 900;
    color: #ff714b;
  }

  .winner-banner {
    margin-top: 24px;
    background: #c8ff3d;
    color: #101828;
    font-family: 'JetBrains Mono', monospace;
    font-size: 13px;
    font-weight: 700;
    padding: 10px 24px;
    border-radius: 14px;
    border: 2px solid #101828;
  }
</style>

<div class="duel-screen">
  <div class="duel-card">
    <div class="duel-tag">⚔️ ✦ BATALHA DE CARTAS ✦</div>

    <div class="vs-row">
      <div>
        <div class="card-box">
          <img src="{{data.cardA.image}}" alt="{{data.cardA.name}}" />
        </div>
      </div>

      <div class="vs-badge">VS</div>

      <div>
        <div class="card-box" style="border-color:#ff714b;">
          <img src="{{data.cardB.image}}" alt="{{data.cardB.name}}" />
        </div>
      </div>
    </div>

    <div class="winner-banner">
      🏆 VENCEDOR: @{{data.winner}} ({{data.winnerHP}} HP RESTANTE)
    </div>
  </div>
</div>
```
