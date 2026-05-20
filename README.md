/* Configurações Globais e Variáveis */
:root {
    --primary-green: #2d6a4f;    /* Verde escuro para textos e destaques */
    --accent-green: #40916c;     /* Verde médio para botões */
    --light-green: #d8f3dc;      /* Verde muito claro para fundos de seção */
    --pure-white: #ffffff;
    --soft-gray: #f8f9fa;
    --text-main: #1b4332;
    --shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
    line-height: 1.6;
    color: var(--text-main);
    background-color: var(--pure-white);
}

/* Header e Navegação */
header {
    background-color: var(--pure-white);
    padding: 1rem 5%;
    display: flex;
    justify-content: space-between;
    align-items: center;
    box-shadow: var(--shadow);
    position: sticky;
    top: 0;
    z-index: 1000;
}

.logo {
    font-size: 1.5rem;
    font-weight: bold;
    color: var(--primary-green);
}

nav ul {
    display: flex;
    list-style: none;
    gap: 20px;
}

nav a {
    text-decoration: none;
    color: var(--primary-green);
    font-weight: 500;
    transition: color 0.3s;
}

nav a:hover {
    color: var(--accent-green);
}

/* Seção Hero (Destaque inicial) */
.hero {
    padding: 80px 5%;
    background: linear-gradient(135deg, var(--pure-white) 60%, var(--light-green) 100%);
    display: flex;
    align-items: center;
    gap: 40px;
}

.hero-content h1 {
    font-size: 3rem;
    color: var(--primary-green);
    margin-bottom: 20px;
}

/* Grid Informativo (Cards) */
.info-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 30px;
    padding: 60px 5%;
    background-color: var(--soft-gray);
}

.card {
    background: var(--pure-white);
    padding: 30px;
    border-radius: 12px;
    border-left: 5px solid var(--accent-green);
    box-shadow: var(--shadow);
    transition: transform 0.3s ease;
}

.card:hover {
    transform: translateY(-5px);
}

.card h3 {
    margin-bottom: 15px;
    color: var(--primary-green);
}

/* Botões Modernos */
.btn-primary {
    background-color: var(--accent-green);
    color: white;
    padding: 12px 25px;
    border: none;
    border-radius: 8px;
    cursor: pointer;
    font-size: 1rem;
    transition: background 0.3s;
}

.btn-primary:hover {
    background-color: var(--primary-green);
}

/* Responsividade */
@media (max-width: 768px) {
    .hero {
        flex-direction: column;
        text-align: center;
    }
    
    nav ul {
        display: none; /* Idealmente trocar por um menu hambúrguer */
    }
}