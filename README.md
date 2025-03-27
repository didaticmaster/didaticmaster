<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>DidaticaMaster - Materiais Pedagógicos Premium</title>
    <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap">
    <style>
        /* Reset e Variáveis */
        :root {
            --primary: #2563eb;    /* Azul vibrante */
            --secondary: #1e40af;  /* Azul mais escuro */
            --accent: #f59e0b;    /* Laranja destaque */
            --light: #f8fafc;     /* Fundo claro */
            --dark: #1e293b;      /* Texto escuro */
            --gray: #94a3b8;      /* Cinza para textos secundários */
            --white: #ffffff;     /* Branco puro */
            --shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -1px rgba(0, 0, 0, 0.06);
            --rounded: 12px;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Poppins', sans-serif;
            background-color: var(--light);
            color: var(--dark);
            line-height: 1.6;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* Header */
        header {
            background-color: var(--white);
            box-shadow: var(--shadow);
            padding: 20px 0;
            position: sticky;
            top: 0;
            z-index: 100;
        }
        
        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            font-size: 24px;
            font-weight: 700;
            color: var(--primary);
            text-decoration: none;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .logo-icon {
            color: var(--accent);
            font-size: 28px;
        }
        
        /* Hero Section */
        .hero {
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            color: var(--white);
            padding: 100px 0;
            text-align: center;
            position: relative;
            overflow: hidden;
        }
        
        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url('https://images.unsplash.com/photo-1523050854058-8df90110c9f1?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80') no-repeat center center/cover;
            opacity: 0.1;
        }
        
        .hero-content {
            position: relative;
            z-index: 2;
            max-width: 800px;
            margin: 0 auto;
        }
        
        .hero h1 {
            font-size: 2.8rem;
            margin-bottom: 20px;
            font-weight: 700;
            line-height: 1.2;
        }
        
        .hero p {
            font-size: 1.2rem;
            margin-bottom: 30px;
            opacity: 0.9;
        }
        
        /* Botões */
        .btn {
            display: inline-block;
            padding: 12px 30px;
            border-radius: var(--rounded);
            text-decoration: none;
            font-weight: 600;
            font-size: 1rem;
            transition: all 0.3s ease;
            text-align: center;
        }
        
        .btn-primary {
            background-color: var(--accent);
            color: var(--white);
            box-shadow: var(--shadow);
        }
        
        .btn-primary:hover {
            background-color: #e67e22;
            transform: translateY(-2px);
            box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -2px rgba(0, 0, 0, 0.05);
        }
        
        /* Seção de Destaques */
        .features {
            padding: 80px 0;
            background-color: var(--white);
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 50px;
        }
        
        .section-title h2 {
            font-size: 2rem;
            color: var(--primary);
            margin-bottom: 15px;
        }
        
        .section-title p {
            color: var(--gray);
            max-width: 600px;
            margin: 0 auto;
        }
        
        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .feature-card {
            background-color: var(--white);
            border-radius: var(--rounded);
            padding: 30px;
            box-shadow: var(--shadow);
            transition: transform 0.3s ease;
            text-align: center;
        }
        
        .feature-card:hover {
            transform: translateY(-10px);
        }
        
        .feature-icon {
            font-size: 40px;
            color: var(--primary);
            margin-bottom: 20px;
        }
        
        .feature-card h3 {
            font-size: 1.3rem;
            margin-bottom: 15px;
            color: var(--dark);
        }
        
        .feature-card p {
            color: var(--gray);
        }
        
        /* Seção de Produtos */
        .products {
            padding: 80px 0;
            background-color: var(--light);
        }
        
        .product-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 30px;
        }
        
        .product-card {
            background-color: var(--white);
            border-radius: var(--rounded);
            overflow: hidden;
            box-shadow: var(--shadow);
            transition: all 0.3s ease;
        }
        
        .product-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 10px 10px -5px rgba(0, 0, 0, 0.04);
        }
        
        .product-image {
            height: 200px;
            background-size: cover;
            background-position: center;
        }
        
        .product-info {
            padding: 20px;
        }
        
        .product-info h3 {
            font-size: 1.2rem;
            color: var(--dark);
            margin-bottom: 10px;
        }
        
        .product-info p {
            color: var(--gray);
            margin-bottom: 15px;
            font-size: 0.9rem;
        }
        
        .price {
            font-size: 1.3rem;
            font-weight: 700;
            color: var(--primary);
            margin: 15px 0;
        }
        
        /* Depoimentos */
        .testimonials {
            padding: 80px 0;
            background-color: var(--white);
        }
        
        .testimonial-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .testimonial-card {
            background-color: var(--white);
            padding: 30px;
            border-radius: var(--rounded);
            box-shadow: var(--shadow);
            border: 1px solid rgba(0, 0, 0, 0.05);
        }
        
        .testimonial-text {
            font-style: italic;
            margin-bottom: 20px;
            color: var(--dark);
        }
        
        .testimonial-author {
            display: flex;
            align-items: center;
            gap: 15px;
        }
        
        .author-avatar {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            background-color: var(--primary);
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--white);
            font-weight: bold;
        }
        
        .author-info h4 {
            font-size: 1rem;
            color: var(--dark);
        }
        
        .author-info p {
            font-size: 0.8rem;
            color: var(--gray);
        }
        
        /* CTA Section */
        .cta {
            padding: 80px 0;
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            color: var(--white);
            text-align: center;
        }
        
        .cta h2 {
            font-size: 2rem;
            margin-bottom: 20px;
        }
        
        .cta p {
            max-width: 600px;
            margin: 0 auto 30px;
            opacity: 0.9;
        }
        
        /* Footer */
        footer {
            background-color: var(--dark);
            color: var(--white);
            padding: 50px 0 20px;
        }
        
        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 30px;
            margin-bottom: 40px;
        }
        
        .footer-column h3 {
            font-size: 1.2rem;
            margin-bottom: 20px;
            color: var(--white);
        }
        
        .footer-column ul {
            list-style: none;
        }
        
        .footer-column ul li {
            margin-bottom: 10px;
        }
        
        .footer-column ul li a {
            color: var(--gray);
            text-decoration: none;
            transition: color 0.3s ease;
        }
        
        .footer-column ul li a:hover {
            color: var(--white);
        }
        
        .copyright {
            text-align: center;
            padding-top: 20px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: var(--gray);
            font-size: 0.9rem;
        }
        
        /* Responsividade */
        @media (max-width: 768px) {
            .hero h1 {
                font-size: 2rem;
            }
            
            .hero p {
                font-size: 1rem;
            }
        }
    </style>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
</head>
<body>
    <!-- Cabeçalho -->
    <header>
        <div class="container header-content">
            <a href="#" class="logo">
                <i class="fas fa-book-open logo-icon"></i>
                <span>DidaticaMaster</span>
            </a>
            <nav>
                <a href="#products" style="color: var(--primary); font-weight: 500;">Produtos</a>
            </nav>
        </div>
    </header>
    
    <!-- Seção Hero -->
    <section class="hero">
        <div class="hero-content">
            <h1>Materiais Pedagógicos que Transformam a Educação</h1>
            <p>Apostilas, planos de aula e recursos didáticos criados por especialistas para elevar o nível do ensino em sua escola.</p>
            <a href="#products" class="btn btn-primary">Conheça Nossos Produtos</a>
        </div>
    </section>
    
    <!-- Seção de Destaques -->
    <section class="features">
        <div class="container">
            <div class="section-title">
                <h2>Por que escolher nossos materiais?</h2>
                <p>Desenvolvidos por educadores para educadores, com foco em resultados reais em sala de aula.</p>
            </div>
            
            <div class="features-grid">
                <div class="feature-card">
                    <i class="fas fa-check-circle feature-icon"></i>
                    <h3>Alinhado à BNCC</h3>
                    <p>Todos os conteúdos seguem as diretrizes da Base Nacional Comum Curricular.</p>
                </div>
                
                <div class="feature-card">
                    <i class="fas fa-lightbulb feature-icon"></i>
                    <h3>Pronto para Uso</h3>
                    <p>Materiais que você pode aplicar imediatamente em suas aulas.</p>
                </div>
                
                <div class="feature-card">
                    <i class="fas fa-graduation-cap feature-icon"></i>
                    <h3>Resultados Comprovados</h3>
                    <p>Metodologia testada e aprovada por milhares de educadores.</p>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Seção de Produtos -->
    <section class="products" id="products">
        <div class="container">
            <div class="section-title">
                <h2>Nossos Materiais</h2>
                <p>Conheça nossos produtos cuidadosamente desenvolvidos para educadores.</p>
            </div>
            
            <div class="product-grid">
                <div class="product-card">
                    <div class="product-image" style="background-image: url('https://images.unsplash.com/photo-1635070041078-e363dbe005cb?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80');"></div>
                    <div class="product-info">
                        <h3>Apostila de Alfabetização</h3>
                        <p>Método comprovado para alfabetização infantil com atividades lúdicas.</p>
                        <div class="price">R$ 89,90</div>
                        <a href="https://wa.me/55555999811379?text=Olá!%20Gostaria%20de%20comprar%20a%20Apostila%20de%20Alfabetização" class="btn btn-primary" target="_blank">Comprar Agora</a>
                    </div>
                </div>
                
                <div class="product-card">
                    <div class="product-image" style="background-image: url('https://images.unsplash.com/photo-1503676260728-1c00da094a0b?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80');"></div>
                    <div class="product-info">
                        <h3>Planos de Aula BNCC</h3>
                        <p>Planos alinhados à Base Nacional Comum Curricular para Educação Infantil.</p>
                        <div class="price">R$ 129,90</div>
                        <a href="https://wa.me/55555999811379?text=Olá!%20Gostaria%20de%20comprar%20os%20Planos%20de%20Aula%20BNCC" class="btn btn-primary" target="_blank">Comprar Agora</a>
                    </div>
                </div>
                
                <div class="product-card">
                    <div class="product-image" style="background-image: url('https://images.unsplash.com/photo-1606326608606-aa0b62935f2b?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80');"></div>
                    <div class="product-info">
                        <h3>Kit Jogos Pedagógicos</h3>
                        <p>Coleção de 15 jogos para desenvolver habilidades cognitivas.</p>
                        <div class="price">R$ 149,90</div>
                        <a href="https://wa.me/55555999811379?text=Olá!%20Gostaria%20de%20comprar%20o%20Kit%20Jogos%20Pedagógicos" class="btn btn-primary" target="_blank">Comprar Agora</a>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Depoimentos -->
    <section class="testimonials">
        <div class="container">
            <div class="section-title">
                <h2>O que dizem nossos clientes</h2>
                <p>Veja a opinião de educadores que já usam nossos materiais.</p>
            </div>
            
            <div class="testimonial-grid">
                <div class="testimonial-card">
                    <p class="testimonial-text">"Os materiais da DidaticaMaster revolucionaram minha forma de ensinar. Meus alunos estão muito mais engajados e os resultados melhoraram significativamente."</p>
                    <div class="testimonial-author">
                        <div class="author-avatar">A</div>
                        <div class="author-info">
                            <h4>Ana Clara</h4>
                            <p>Professora do 1º ano</p>
                        </div>
                    </div>
                </div>
                
                <div class="testimonial-card">
                    <p class="testimonial-text">"Finalmente encontrei apostilas que realmente seguem as diretrizes da BNCC. Economizei horas de planejamento e minhas aulas estão muito mais ricas."</p>
                    <div class="testimonial-author">
                        <div class="author-avatar">C</div>
                        <div class="author-info">
                            <h4>Carlos Eduardo</h4>
                            <p>Coordenador Pedagógico</p>
                        </div>
                    </div>
                </div>
                
                <div class="testimonial-card">
                    <p class="testimonial-text">"Comprei o kit de jogos e foi o melhor investimento que fiz para minha escola este ano. As crianças adoram e aprendem brincando."</p>
                    <div class="testimonial-author">
                        <div class="author-avatar">M</div>
                        <div class="author-info">
                            <h4>Mariana Silva</h4>
                            <p>Diretora Escolar</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <!-- CTA -->
    <section class="cta">
        <div class="container">
            <h2>Pronto para transformar suas aulas?</h2>
            <p>Adquira agora nossos materiais e leve sua prática pedagógica para o próximo nível.</p>
            <a href="#products" class="btn btn-primary">Ver Produtos</a>
        </div>
    </section>
    
    <!-- Rodapé -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-column">
                    <h3>DidaticaMaster</h3>
                    <p>Materiais pedagógicos de alta qualidade para educadores comprometidos com a excelência no ensino.</p>
                </div>
                
                <div class="footer-column">
                    <h3>Produtos</h3>
                    <ul>
                        <li><a href="#products">Apostilas</a></li>
                        <li><a href="#products">Planos de Aula</a></li>
                        <li><a href="#products">Jogos Pedagógicos</a></li>
                    </ul>
                </div>
                
                <div class="footer-column">
                    <h3>Contato</h3>
                    <ul>
                        <li><a href="https://wa.me/55555999811379" target="_blank">WhatsApp</a></li>
                        <li><a href="mailto:contato@didaticamaster.com.br">E-mail</a></li>
                    </ul>
                </div>
            </div>
            
            <div class="copyright">
                <p>&copy; 2023 DidaticaMaster. Todos os direitos reservados.</p>
            </div>
        </div>
    </footer>
</body>
</html>
