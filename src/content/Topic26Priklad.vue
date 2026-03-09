<template>
  <div class="topic-content-wrapper">
    <section class="glass-panel content-section">
      <h2>Agilní řízení: Kanban nástěnka v praxi</h2>
      <p>Představujeme Vám reálnou virtuální simulaci <strong>Kanbanu</strong>, což je vizuální pomůcka v Agilním řízení od firmy Toyota. Každý programátor přesně vidí úkoly celého svého týmu pěkně sepsané na jednom místě napříč životními cykly vývoje.</p>
      
      <div style="background: #e2e8f0; color: #333; padding: 10px 20px; font-weight: bold; border-radius: 8px; margin: 2rem 0 1rem 0; box-shadow: 0 4px 6px -1px rgba(0,0,0,0.1);">
        Sprint 3: Vydání přihlašovacího síně | Časový limit: zbývá 8 dní
      </div>

      <!-- KANBAN BOARD MOCKUP -->
      <div class="kanban-board">
        
        <!-- Column 1 -->
        <div class="kanban-column">
          <div class="kanban-header ToDo">To Do (K udělání) <span>2</span></div>
          <div class="kanban-card">
            <h4>#104 Oprava Patičky</h4>
            <p>Text vpravo dole přetéká na mobilních telefonech z displeje.</p>
            <div class="card-footer">
              <span class="tag low">Low Prio</span>
              <div class="assignee user-p">P</div>
            </div>
          </div>
          <div class="kanban-card">
            <h4>#105 Integrace Plateb</h4>
            <p>Napojení na API mBank a ČSOB.</p>
            <div class="card-footer">
              <span class="tag high">High Prio</span>
              <div class="assignee user-m">M</div>
            </div>
          </div>
        </div>

        <!-- Column 2 -->
        <div class="kanban-column">
          <div class="kanban-header InProgress">In Progress (Tvorba) <span>1</span></div>
          <div class="kanban-card active">
            <h4>#102 Tlačítko 'Přihlásit'</h4>
            <p>Ztrávili jsme na tom už tři dny, aktuálně navrhuji CSS gradienty pro stav najetí (hover state).</p>
            <div class="card-footer">
              <span class="tag tag-dev">Frontend</span>
              <div class="assignee user-t">T</div>
            </div>
          </div>
        </div>

        <!-- Column 3 -->
        <div class="kanban-column">
          <div class="kanban-header Testing">Testing (Testuji) <span>1</span></div>
          <div class="kanban-card alert-card">
            <h4>#101 Bezpečnost Hesla</h4>
            <p>Šifrování do DB již funguje trvale u mě local, prosím kontrolu na Test serveru.</p>
            <div class="card-footer">
              <span class="tag tag-db">Backend</span>
              <div class="assignee user-p">P</div>
            </div>
          </div>
        </div>
        
        <!-- Column 4 -->
        <div class="kanban-column">
          <div class="kanban-header Done">Done (Hotovo) <span>1</span></div>
           <div class="kanban-card finished">
            <h4 style="text-decoration: line-through;">#99 Získání DOMény</h4>
            <p>Objednána a zaplacena adresa www.okruhy.xyz</p>
            <div class="card-footer">
              <span class="tag tag-admin">Admin</span>
              <div class="assignee user-m">M</div>
            </div>
          </div>
        </div>

      </div>

      <div class="notice" style="margin-top: 2rem;">
        Zkratky Scrum metodologie: Tým má každý den ráno krátkou 15 minutovou <strong>Daily schůzku</strong> u této obrazovky. Každý člen týmu řekne 3 věci: Co dělal včera (#102 Tlačítko), Co bude dělat dnes (CSS gradient), a jestli mu v něčem někdo brání. Programátoři si tak sami rozeberou kartičky ze sloupce TO-DO na In Progress systémem vlastního naplánování.
      </div>
    </section>
  </div>
</template>

<style scoped>
@import './topic-styles.css';

/* Kanban specific styles to impress */
.kanban-board {
  display: flex;
  gap: 1.5rem;
  overflow-x: auto;
  padding-bottom: 1rem;
  margin-top: 1rem;
}

.kanban-column {
  flex: 1;
  min-width: 250px;
  background: rgba(15, 23, 42, 0.4);
  border-radius: 8px;
  border: 1px solid rgba(255, 255, 255, 0.05);
  display: flex;
  flex-direction: column;
  gap: 1rem;
  padding: 10px;
}

.kanban-header {
  font-weight: 700;
  font-size: 1rem;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding-bottom: 0.5rem;
  border-bottom: 2px solid;
}

.kanban-header span {
  background: rgba(255,255,255,0.1);
  padding: 2px 8px;
  border-radius: 12px;
  font-size: 0.8em;
}

.ToDo { border-bottom-color: #94a3b8; color: #cbd5e1; }
.InProgress { border-bottom-color: #3b82f6; color: #60a5fa; }
.Testing { border-bottom-color: #f59e0b; color: #fbbf24; }
.Done { border-bottom-color: #10b981; color: #34d399; }

.kanban-card {
  background: rgba(30, 41, 59, 1);
  border-radius: 6px;
  padding: 12px;
  cursor: grab;
  border: 1px solid rgba(255,255,255,0.1);
  box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -1px rgba(0, 0, 0, 0.06);
  transition: transform 0.2s;
}

.kanban-card:hover {
  transform: translateY(-2px);
  border-color: rgba(255,255,255,0.2);
}

.kanban-card.active { border-left: 3px solid #3b82f6; }
.kanban-card.alert-card { border-left: 3px solid #f59e0b; }
.kanban-card.finished { opacity: 0.6; }

.kanban-card h4 {
  margin: 0 0 8px 0;
  font-size: 0.95em;
  color: #f8fafc;
}

.kanban-card p {
  margin: 0 0 12px 0;
  font-size: 0.8em;
  color: #94a3b8;
  line-height: 1.4;
}

.card-footer {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.tag {
  font-size: 0.7em;
  padding: 3px 8px;
  border-radius: 4px;
  font-weight: 600;
}
.low { background: #334155; color: #cbd5e1; }
.high { background: rgba(239, 68, 68, 0.2); color: #fca5a5; }
.tag-dev { background: rgba(59, 130, 246, 0.2); color: #93c5fd; }
.tag-db { background: rgba(168, 85, 247, 0.2); color: #d8b4fe; }
.tag-admin { background: rgba(16, 185, 129, 0.2); color: #a7f3d0; }

.assignee {
  width: 24px;
  height: 24px;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 0.7em;
  font-weight: bold;
  color: white;
}
.user-p { background: #ef4444; }
.user-m { background: #3b82f6; }
.user-t { background: #10b981; }

</style>
