# saude-
Crie um site com isso: <style>
  :root {
    --primary-blue: #0066ff;
    --dark-blue: #0a3560;
    --bg-light: #f4f7fb;
    --card-bg: #ffffff;
    --text-color: #1e293b;
    --text-muted: #64748b;
    --green-status: #10b981;
    --yellow-status: #f59e0b;
    --radius: 16px;
  }

  body {
    font-family: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
    background-color: #eef2f6;
    padding: 20px;
  }

  .app-layout {
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
    justify-content: center;
  }

  .saude-card {
    width: 380px;
    background-color: var(--bg-light);
    border-radius: 24px;
    padding: 20px;
    box-shadow: 0 10px 25px rgba(0, 0, 0, 0.08);
    color: var(--text-color);
  }

  /* Cabeçalho e Títulos */
  .app-header h2 { font-size: 20px; font-weight: 800; color: var(--dark-blue); margin: 0 0 4px 0; }
  .app-header p { font-size: 13px; color: var(--text-muted); margin: 0 0 16px 0; }
  .section-title { display: flex; justify-content: space-between; align-items: center; font-size: 15px; font-weight: 700; margin: 16px 0 10px 0; }
  .section-title a { color: var(--primary-blue); font-size: 12px; text-decoration: none; font-weight: 600; }

  /* Login Card */
  .login-card { background: white; border-radius: var(--radius); padding: 24px; text-align: center; }
  .login-card .logo-icon { width: 48px; height: 48px; background: #e0edff; border-radius: 12px; display: inline-flex; align-items: center; justify-content: center; color: var(--primary-blue); font-size: 24px; margin-bottom: 12px; }
  .login-card h3 { font-size: 24px; color: var(--dark-blue); margin: 4px 0; }
  .btn-primary { width: 100%; background: var(--primary-blue); color: white; border: none; padding: 12px; border-radius: 10px; font-weight: 700; cursor: pointer; margin-top: 12px; }
  .btn-secondary { width: 100%; background: #e0edff; color: var(--primary-blue); border: none; padding: 12px; border-radius: 10px; font-weight: 700; cursor: pointer; margin-top: 8px; }

  /* Item Acompanhamento / Solicitação */
  .item-card { background: var(--card-bg); padding: 14px; border-radius: var(--radius); display: flex; justify-content: space-between; align-items: center; margin-bottom: 10px; }
  .badge { padding: 4px 10px; border-radius: 20px; font-size: 11px; font-weight: 600; }
  .badge-yellow { background: #fef3c7; color: #d97706; }
  .badge-blue { background: #e0f2fe; color: #0284c7; }
  .badge-green { background: #d1fae5; color: #059669; }

  /* Assistente Virtual */
  .assistant-card { background: white; border-radius: var(--radius); padding: 16px; margin-top: 16px; }
  .chat-bubble { background: #e0edff; padding: 12px; border-radius: 12px; font-size: 13px; color: var(--dark-blue); margin: 10px 0; }
  .chat-input { display: flex; gap: 8px; }
  .chat-input input { flex: 1; padding: 8px 12px; border: 1px solid #cbd5e1; border-radius: 20px; font-size: 12px; }

  /* Lista de Orientações (FAQ) */
  .faq-item { background: white; padding: 14px; border-radius: 12px; font-size: 13px; font-weight: 600; margin-bottom: 8px; cursor: pointer; color: var(--dark-blue); }
</style>

<div class="app-layout">
  
  <!-- ECRÃ 1: LOGIN -->
  <div class="saude-card">
    <div class="login-card">
      <div class="logo-icon">💙</div>
      <span style="font-size: 11px; color: var(--primary-blue); font-weight: 700; letter-spacing: 0.5px;">JORNADA DE SAÚDE PÚBLICA</span>
      <h3>Saúde+</h3>
      <p style="font-size: 13px; color: var(--text-muted);">Acompanhe sua jornada de saúde.</p>
      
      <button class="btn-primary">Entrar com CPF</button>
      <div style="margin-top: 10px; font-size: 13px; font-weight: 600; color: var(--dark-blue);">Entrar com conta Gov.br</div>
      <button class="btn-secondary">Primeiro acesso</button>
    </div>
  </div>

  <!-- ECRÃ 2: PAINEL PRINCIPAL COM "PESSOAS QUE ACOMPANHO" -->
  <div class="saude-card">
    <div class="app-header">
      <h2>Olá, Maria 👋</h2>
      <p>Veja como está sua jornada de saúde.</p>
    </div>

    <div class="section-title">
      <span>Minhas solicitações</span>
      <a href="#">Ver jornada</a>
    </div>
    
    <div class="item-card">
      <div>
        <!-- ...conteúdo das solicitações... -->
        <strong style="font-size: 14px;">Cardiologia</strong>
        <div style="font-size: 11px; color: var(--text-muted);">Solicitado em: 12/08/2026</div>
      </div>
      <span class="badge badge-blue">• Em regulação</span>
    </div>

    <!-- Pessoas que acompanho -->
    <div class="section-title">
      <span>Pessoas que acompanho</span>
      <a href="#">Privacidade</a>
    </div>

    <div class="item-card">
      <div style="display: flex; gap: 10px; align-items: center;">
        <div style="width: 32px; height: 32px; background: #e8f5e9; color: #2e7d32; border-radius: 50%; display: flex; align-items: center; justify-content: center; font-weight: bold;">A</div>
        <div>
          <strong style="font-size: 13px;">Minha mãe — Ana</strong>
          <div style="font-size: 11px; color: var(--text-muted);">Consulta: Neurologia</div>
        </div>
      </div>
      <span class="badge badge-yellow">• Aguardando agendamento</span>
    </div>
  </div>

  <!-- ECRÃ 3: ORIENTAÇÕES & ASSISTENTE VIRTUAL -->
  <div class="saude-card">
    <div class="section-title"><span>Apoio e Orientações</span></div>
    
    <div class="faq-item">Perdi meu agendamento</div>
    <div class="faq-item">Meu telefone mudou</div>
    <div class="faq-item">Não consegui comparecer</div>
    <div class="faq-item">Tenho uma dúvida sobre minha solicitação</div>

    <!-- Assistente Saúde+ -->
    <div class="assistant-card">
      <strong style="font-size: 14px; color: var(--dark-blue);">💬 Assistente Saúde+</strong>
      <div class="chat-bubble">
        Olá! Posso ajudar com informações administrativas sobre sua solicitação.
      </div>
      <div class="chat-input">
        <input type="text" placeholder="Escreva sua dúvida">
        <button style="background: var(--primary-blue); color: white; border: none; border-radius: 50%; width: 30px; height: 30px;">➤</button>
      </div>
    </div>
  </div>

</div>