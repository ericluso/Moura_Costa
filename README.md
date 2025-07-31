<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Header Responsivo - Moura Costa</title>

  <!-- Fonte Inter via Google Fonts -->
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;800&display=swap" rel="stylesheet">

  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Inter', sans-serif;
    }

    .header {
    display: flex;
    flex-direction: column; /* empilha os elementos verticalmente */
    align-items: stretch;
    justify-content: flex-start;
    position: relative;
    background-image: url('Moura_Costa_completo.png');
    background-size: cover;
    background-position: center;
    color: white;
    min-height: 100vh;
    padding: 58px;
    overflow: hidden;
    flex-wrap: wrap;
    }
        .header::before {
      content: "";
      position: absolute;
      top: 0;
      left: 0;
      height: 100%;
      width: 100%;
      background: rgba(0, 0, 0, 0.466);
      z-index: 2;
    }

    .header > * {
      position: relative;
      z-index: 2;
    }

    .nav {
      /* position: absolute;
      top: 20px;
      left: 60px;
      */ 
      display: flex;
      gap: 20px;
      z-index: 2;
    }

    .nav a {
      color: white;
      text-decoration: none;
      font-weight: 400;
      font-size: 18px;
      transition: color 0.3s;
    }

    .nav a:hover {
      color: #ffd7c2;
    }

    .content {
      flex: 1 1 25%;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      text-align: center;
    }

    .content h1 {
      font-size: 52px;
      margin-bottom: 8px;
      font-weight: 800;
      text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.5);
    }

    .content p {
      line-height: 1.30;
      font-size: 20px;
      margin-bottom: 20px;
      max-width: 610px;
      text-align: justify;
      text-shadow: 5px 1px 4px rgba(0, 0, 0, 0.4);
    }

    .button {
      padding: 15px 30px;
      background-color: #0212f1;
      color: white;
      font-weight: bold;
      border: none;
      border-radius: 25px;
      text-decoration: none;
      box-shadow: 0 8px 15px rgba(0, 0, 0, 0.3);
      transition: background 0.3s;
      margin-top: 15px;
      display: inline-block;
    }

    .button:hover {
      background-color: #11032e;
    }

    .button-consultor {
    background-color: #131f09; /* cor diferente, exemplo: laranja */
    color: #fff;
   }

.button-consultor:hover {
  background-color: #e65100; /* cor ao passar o mouse */
}

/*    .image-side {
      flex: 4.2 4.2 160%;
      background-image: url('laptop.png');
      background-size: contain;
      background-repeat: no-repeat;
      background-position: right;
      height: 900px;
    }
/*
    /* Seção Escopo */
    #escopo {
      background: #0354ea;
      text-align: left;
      align-items: flex-start;
      justify-content: flex-start;
      color: #f0ebebc5;
      padding: 60px 40px;
      text-align: left;
    }

    #escopo h1 {
      font-size: 36px;
      margin-bottom: 15px;
    }

    #escopo p {
      font-size: 20px;
      line-height: 1.3;
      margin-bottom: 20px;
    }

    /* Segundo bloco */

    #escopo.escopo-flex {
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 40px;
    padding: 60px 40px;
    }

    .escopo-texto {
    flex: 1 1 60%;
    text-align: justify-right;
    line-height: 1.45;
    }

    .escopo-texto_bloco_03 {
    flex: 1 1 60%;
    text-align: justify;
    line-height: 1.1;
    text-align: center;
    color:rgb(4, 4, 4)
    }

    .escopo-texto_bloco_04 {
    flex: 1 1 60%;
    text-align: justify;
    line-height: 1.1;
    text-align: center;
    color:rgb(3, 5, 96)
    }

    .escopo-texto_bloco_05 {
    flex: 1 1 60%;
    text-align: justify-right;
    line-height: 1.3;
    text-align: center;
    color:rgb(225, 225, 225)
    }


    /* Terceiro bloco */


    /* Container principal de cada etiqueta */
    .etiqueta {
    width: 100%;
    max-width: 520px;
    display: flex;                  /* Alinha a imagem e texto lado a lado */
    align-items: flex-start;        /* Alinha os itens ao topo */
    background-color: #f5f5f5;      /* Cor de fundo clara */
    border-radius: 12px;            /* Bordas arredondadas */
    padding: 16px;
    margin-bottom: 16px;
    box-shadow: 0 2px 6px rgba(0,0,0,0.1); /* Sombra leve */
    }

    /* Estilo da imagem */
    .icone {
    width: 50px;
    height: auto;
    margin-right: 16px;             /* Espaço entre imagem e texto */
    }

    /* Texto da etiqueta */
    .texto h3 {
    margin: 0;
    font-size: 16px;
    font-weight: bold;
    color: #333;
    }

    .texto p {
    margin: 4px 0 0 0;
    font-size: 14px;
    color: #666;
    }
    /* Estilo do botão */

    .escopo-img-direita {
    flex: 1 1 40%;
    display: flex;
    justify-content: flex-end;
    align-items: center;
    }

    .escopo-img-direita img {
    max-width: 480px;
    width: 120%;
    height: auto;
    border-radius: 0px;
    box-shadow: 0 4px 16px rgba(0,0,0,0.10);
    }

    @media (max-width: 768px) {
      .header {
        flex-direction: column;
        padding: 40px 20px;
      }

      .nav {
        flex-direction: row;
        position: static;
        justify-content: center;
        margin-bottom: 50px;
      }

      .content {
        text-align: right;
        flex: none;
        width: 100%;
      }

    .image-side {
    flex: 4.2 4.2 180%;
    background-image: url('laptop.png');
    background-size: cover;      /* faz a imagem ocupar todo o espaço */
    background-repeat: no-repeat;
    background-position: center right;
    width: 180%;                 /* aumenta a largura */
    height: 1200px;              /* aumenta a altura */
    max-width: none;
    }   
    }

.bloco-imagem {
  width: 100%;
  padding: 0;
  margin: 0;
  display: flex;
  opacity: 0.92;
  justify-content: center;
  background: transparent; /* ou defina uma cor de fundo se quiser */
}


.bloco-imagem img {
  width: 100%;
  max-width: 120vw;
  height: auto;
  display: block;
}

/* IMAGEM - componentes e etiquetas do bloco 4 */ 

.icones-container {
  display: flex;
  justify-content: center;
  align-items: flex-end;
  gap: 30px;
  padding: 20px;
  flex-wrap: wrap;
}

.icone-item {
  text-align: center;
  width: 100px;
  position: relative;
}

.icone-item img {
  width: 138px;
  height: 172px;
}

.icone-item p {
  position: absolute;
  top: -20px;
  left: 50%;
  transform: translateX(-50%) rotate(-15deg);
  color: #ffffff;
  font-size: 0.85rem;
  font-weight: bold;
  white-space: nowrap;
}

/* IMAGEM - componentes e etiquetas do bloco 5 */

/* Analisar amanhã sobre como inserir apenas o entorno, com texto no interior. */

.escopo-flex {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 40px;
  padding: 60px 40px;
}

.escopo-img-esquerda_bloco_05 {
  flex: 1 1 40%;
  display: flex;
  justify-content: flex-start;
  align-items: center;
}

.escopo-img-esquerda_bloco_05 img {
  max-width: 380px;
  width: 100%;
  height: auto;
  border-radius: 0;
  box-shadow: 0 4px 16px rgba(0,0,0,0.10);
}

.escopo-texto-direita_bloco_05 {
  flex: 1 1 60%;
  text-align: left;
  align-items: flex-end;
}

.escopo-texto-direita h1,
.escopo-texto-direita h2,
.escopo-texto-direita p {
  text-align: left;
}



/* Estilo do botão no bloco 6 * - configuração JsCript/ */ 

.carrossel-container {
  position: relative;
  width: 120%;
  max-width: 950px;
  margin: 0 auto;
  overflow: hidden;
  background-color: #4400ff00;
  padding: 10px 0;
}

.carrossel {
  display: flex;
  transition: transform 1.8s ease-in-out;
}

.slide {
  flex: 0 0 31.1%;
  margin: 0 5px;
  background-color: #4302c600;
  border-radius: 4px;
  padding: 16px;
  display: flex;
  justify-content: center;
  align-items: center;
}

.slide img {
  max-width: 280%;
  max-height: 315px;
  object-fit: contain;
}

.dots {
  text-align: center;
  margin-top: 28px;
}

.dots span {
  display: inline-block;
  width: 12px;
  height: 12px;
  margin: 0 6px;
  background-color: #ccc;
  border-radius: 50%;
  cursor: pointer;
}

.dots .active {
  background-color: #ffffff42;
}

/* IMAGEM - componentes e etiquetas do bloco 7 */

.icones-container-menor {
  display: flex;
  justify-content: center;
  align-items: flex-end;
  gap: 12px;           /* Espaço entre os ícones */
  padding: 10px 0;
}

.icone-item-menor {
  text-align: center;
  width: 250px;         /* Largura menor */
  position: relative;
}

.icone-item-menor img {
  width: 250px;         /* Tamanho menor da imagem */
  height: 270px;
  display: block;
  margin: 0 auto;
}

/* Formulário e adereços */

.orcamento-contato {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  padding: 40px;
  background: linear-gradient(to bottom, #0354ea, #000000);
  color: white;
  font-family: sans-serif;
}

.orcamento, .contato {
  flex: 1 1 45%;
  min-width: 300px;
  margin: 20px;
}

.orcamento h2, .contato h2 {
  font-size: 28px;
  margin-bottom: 10px;
}

.orcamento p, .contato p {
  font-size: 16px;
  margin: 10px 0;
}

form {
  margin-top: 20px;
}

input[type="text"],
input[type="email"],
input[type="tel"] {
  width: 100%;
  padding: 12px;
  margin: 10px 0;
  border-radius: 20px;
  border: 2px solid #ccc;
  font-size: 16px;
}

.input-duplo {
  display: flex;
  gap: 10px;
}

.input-duplo input {
  flex: 1;
}

.button-formulario {
  background-color: #131f09;
  color: #fff;
  padding: 14px 32px;
  border: none;
  border-radius: 30px;
  font-size: 20px;
  font-weight: bold;
  margin-top: 10px;
  cursor: pointer;
  transition: background 0.3s;
  box-shadow: 0 8px 15px rgba(0, 0, 0, 0.1);
}

.button-formulario:hover {
  background-color: #e65100;
}

.icones-contato img,
.redes img {
  width: 79px;
  height: 90px;
  margin-right: 2px;
  border-radius: 20%;
  background-color: rgba(255, 255, 255, 0);
  padding: 0px;
}

.email {
  text-transform: uppercase;
  font-weight: bold;
  font-size: 14px;
}

.redes-title {
  margin-top: 20px;
  font-size: 14px;
}


.contato-equipe {
  margin-top: 30px;
}

.membro {
  display: flex;
  align-items: center;
  margin-bottom: 20px;
}

.membro img {
  width: 60px;
  height: 60px;
  border-radius: 50%;
  object-fit: cover;
  margin-right: 15px;
  border: 2px solid white;
}

.membro .texto {
  color: white;
  font-size: 14px;
}

.membro .nome {
  font-weight: bold;
  margin: 0;
}

.membro .cargo,
.membro .empresa,
.membro .junior {
  margin: 0;
  font-size: 13px;
}

.membro .junior {
  font-weight: bold;
  color: #ccc;
}

/* RODAPÉ */

    .footer {
    background: #211e1e;
    color: #fff;
    padding: 40px 0 20px 0;
}

    .footer-content {
    display: flex;
    align-items: center;
    justify-content: center;
    max-width: 1200px;
    margin: 0 auto;
    gap: 20px;
  padding: 0 40px;
}

.footer-logo {
  height: 60px;
  width: auto;
}

.footer-text {
  font-size: 18px;
}

.footer-p-grande {
 font-size: 26px;
 font-weight: 550;
 text-align: center;

}

.footer-p-pequeno {
  font-size: 10px;
  font-weight: 250;
  text-align: center;
}

/* Container do rodapé */
    .footer_01 {
      background-color: #2a2a2a;
      color: #fff;
      padding: 110px 20px;
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
      font-family: Arial, sans-serif;
      align-items: center;
      gap: 40px;
    }

/* Formatação das três colunas sobre o endereço */ 

/* Colunas */ 

.footer-column {
    flex: 1; 
    min-width: 250px;
    margin: 10px;
}



/* Logo e CNPJ */ 

.footer-logo-img {
  height: 85px; /* ou outro valor maior */
  width: auto;
  display: block;
  margin: 0 auto 16px auto;
  align-items: center;
}

.footer-logo {
  /* mantém as regras de centralização e texto */
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
}
.footer-logo span{
    display: block;
    font-size: 18px;
    font-weight: normal;
    margin-top: 5px;
}

.footer-logo small {
    font-size: 15px;
    color: #9e9e9e;
    display: block;
    margin-top: 15px;
    
}

/*Lista de serviços */

.footer-services ul{
    .footer-services h3{
        font-size: 15px;
        margin-bottom: 15px;
        line-height: 2.8;

    }

}

.footer-services ul li{
    margin-bottom: 5px; 
}

/*Redes Sociais e contato */
.footer-contact {
    display: flex;
    flex-direction: column;
    justify-content: flex-start; 
}

.social-icons {
    display: flex;
    gap: 10px;
    margin-bottom: 10px;

}

.social-icons a {
    background-color: #3b5998;
    color: #fff;
    font-size: 18px;
    width: 32px;
    height: 32px;
    display: flex;
    align-items: center;
    align-content: center;
    justify-content: center;
    border-radius: 25%; 
    text-decoration: none; 

}

.footer-contact p{
    margin: 8px 0; 
    font-size: 14px
}

.footer-contact a{
    color: white;
    text-decoration: none; 
    font-weight: bold; 
}

@media (max-width: 768px){
    .footer_01{
        flex-direction: column;
        align-items: center;
    }
    .footer-column {
        flex: 1; 
        min-width: 180px;
        margin: 0 18px;
        text-align: center; 
    }

    .footer-contact {
        align-items: center;

    }
}


  </style>
</head>
<body>


<!-- HTML Código -->

<header class="header">
  <div class="header-top" style="display: flex; align-items: center; justify-content: space-between; width: 100%;">
    <!-- Logo -->
    <img src="Ativo_04.png" alt="Logo Moura Costa" style="height: 85px;">
    <!-- Navegação -->
    <nav class="nav">
      <a href="#home">Início</a>
      <a href="#sobre">Sobre</a>
      <a href="#servicos">Serviços</a>
      <a href="#contato">Contato</a>
    </nav>
  </div>

<!-- Conteúdo principal -->
<div class="content">
  <h1>MOURA COSTA <h2>Assessoria Financeira</h2></h1>
  <br>
  <p>Mais do que números, entregamos: <br> CLAREZA, CONTROLE E CONFIANÇA<br>para você crescer com SEGURANÇA.</p>
  <br>
  <br>

  <p><strong>Profissionalize agora a gestão financeira <br> da sua empresa.</strong></p>
  <a href="#shop" class="button">Fale com um especialista</a>
</div>

  <!-- Imagem lateral -->
</header>

  <!-- Seção Escopo 1 -->
<section class="escopo-flex" id="escopo" style="background: linear-gradient(90deg, #0354ea 0%, #040009 100%); color: #f0ebebc5; padding: 60px 40px;">
  <div class="escopo-texto">

    <h1><strong>Transforme a Gestão Financeira</strong> 
        <br> da sua empresa <br>
        com <strong>BPO Especializado</strong>
    </h1>

    <br>
    <br>
    <br>

    <p><strong>Organizamos e executamos</strong> toda a <strong>rotina</strong> <br> financeira da sua empresa para que você tenha mais tempo, <br> controle e lucros.</p>
    <p>
      A Moura Costa é especialista em BPO <br> Financeiro para pequenas e médias empresas <br>
      <strong>- com foco em crescimento, organização e decisões baseadas <br> em dados.</strong>
    </p>
    <br>
    <br>
    <a href="#shop" class="button button-consultor">Fale com um consultor</a>
  </div>
  <div class="escopo-img-direita">
    <img src="Monitor_report.jpg" alt="Imagem de Monitoramento Financeiro">
  </div>
</section>

<!-- Novo bloco com background e layout idênticos ao escopo -->
<section class="escopo-flex" id="escopo" style="background: linear-gradient(90deg, #0354ea 0%, #040009 100%); color: #f0ebebc5; padding: 60px 40px;">
  <div class="escopo-texto">
    <h1 style="font-size: 32px; margin-bottom: 30px;">
      Preencha o formulário para ter <br> um time de especialistas <br> cuidando do seu negócio
    </h1>
    <!-- Aqui você pode inserir o formulário futuramente -->

    <br>
    <br>

    <div class="etiqueta">
    <img src="etiqueta_01.png" alt="Ícone de formulário" class="icone", align="right">
    <div class="texto">
        <h3>1. PREENCHA AS INFORMAÇÕES</h3>
        <p>Envie as informações solicitadas ou preencha o formulário enviado.</p>
    </div>
    </div>

    <br>

    <div class="etiqueta">
    <img src="etiqueta_02.png" alt="Ícone de contato" class="icone", align="right">
    <div class="texto">
        <h3>2. RECEBA UM CONTATO</h3>
        <p>Em até 12 horas, um dos nossos especialistas fará contato para agendar <br> uma reunião.</p>
    </div>
    </div>

</div>


  <div class="escopo-img-direita">
    <img src="Ativo_05.png" alt="Imagem de especialistas" style="max-width: 480px; width: 120%; height: auto; border-radius: 0px; box-shadow: 0 4px 16px rgba(0,0,0,0.10);">
  </div>

</section>

<!-- Novo bloco com background e layout idênticos em branco - centralizado -->
<section class="escopo-flex" id="escopo" style="background: linear-gradient(90deg, #fdfdfd 0%, #ffffff 100%); color: #f0ebebc5; padding: 60px 40px;">
  <div class="escopo-texto_bloco_03">
    <h1 style="font-size: 32px; margin-bottom: 30px;">
      Lidar com as <strong> rotinas financeiras, atividades contábeis <br> burocráticas</strong>  e um fluxo de caixa imprevisível pode ser um <br> <strong> verdadeiro desafio </strong> para todos os empresários. <br>
    <br>
    Você se sente <strong><span style="color: rgba(147, 0, 0, 0.84);"> sem tempo? </span> </strong> Que tal trabalhar <span style="color: rgb(39, 38, 0);"> melhor sua gestão</span>, <br>

    para que você <span style="color: rgb(39, 38, 0);"> se preocupe apenas com o que importa? </span> <br>
        <br>
    </h1>

<h3> Na Moura Costa entendemos que seu tempo é valioso, então sua gestão deve ser simplificada e efetiva. <br> Somos uma empresa financeiramente educada, que prepara seu negócio para <span style="color: rgb(39, 38, 0);">o sucesso.</span></h3>
<br>
<h2> <strong>Entenda como podemos te ajudar:</strong></h2>
<br>
<br>

<!-- IMAGEM-->

<div class="icones-container">
  <div class="icone-item">
    <img src="1_um.png" alt="Organizar tempo">
    
  </div>
  <div class="icone-item">
    <img src="2_dois.png" alt="Definir prioridades">
    
  </div>
  <div class="icone-item">
    <img src="3_tres.png" alt="Pagamentos no prazo">
    
  </div>
  <div class="icone-item">
    <img src="4_quatro.png" alt="Relatório financeiro claro">
    
  </div>
</div>

<br>

  <a href="#shop" class="button">Fale com consultor</a>
<br>
<br>
<br>

<h1> Para quem são as nossas soluções? </h1>
<h2> Micro, pequenas e médias empresas, Start-ups ou MEI </h2>

<br>
<h2> <span style="color: rgb(39, 38, 0);">DIFICULDADE PARA ORGANIZAR OS PRAZOS DE PAGAMENTO? </span></h2>
<br>
<h3> Com o fluxo de caixa, você tem <span style="color: rgb(39, 38, 0);">clareza</span> sobre o que entra e sai, evita surpresas e garante <br> <span style="color: rgb(39, 38, 0);">previsibilidade </span> para honrar seus compromissos no prazo. <span style="color: rgb(39, 38, 0);"> Mais controle </span> para você, mais <br> <span style="color: rgb(39, 38, 0);">confiança </span> para seus fornecedores.</h3>

<!-- IMAGEM-->
<br>
<br>

<div class="icones-container-menor">
  <div class="icone-item-menor">
    <img src="site_home_mouracosta_mod1.png" alt="Organizar tempo">
  </div>
  <div class="icone-item-menor">
    <img src="site_home_mouracosta_mod2.png" alt="Definir prioridades">
  </div>
  <div class="icone-item-menor">
    <img src="site_home_mouracosta_mod3.png" alt="Pagamentos no prazo">
  </div>
</div>

<br>
<br>

<a href="#shop" class="button button-consultor">Falar com consultor</a>


    <!-- Aqui você pode inserir o formulário futuramente -->
  </div>

</section>


<!-- Novo bloco com background e layout idênticos em falso - justificado a direita com imagem a esquerda -->
<section class="escopo-flex_bloco_05" id="escopo-consultoria" style="background: linear-gradient(90deg, #090808f1 0%, #0a0a0a 100%); color: #f0ebebc5; padding: 60px 40px;">
  <!-- Título centralizado acima das colunas -->
  <h1 style="font-size: 32px; margin-bottom: 30px; text-align: center; width: 100%;">
    <span style="color: #0354ea;">CONSULTORIA FINANCEIRA ESTRATÉGICA PARA PMES.</span>
  </h1>
  <div style="display: flex; align-items: flex-start; gap: 40px; width: 100%;">
    <!-- Coluna da imagem à esquerda -->
    <div class="escopo-img-esquerda_bloco_05">
      <img src="etiqueta_planos.png" alt="Consultoria Financeira" style="max-width: 380px; width: 100%; height: auto;">
    </div>
    <!-- Coluna do texto à direita -->
    <div class="escopo-texto-direita">
      <h2><span style="color: #0354ea;">Como a Moura Costa ajuda sua empresa a organizar as finanças?</span></h2>
      <p><span style="color: rgb(255, 255, 255);">Assumimos toda a operação com o nosso BPO Financeiro, além de oferecer consultoria estratégica para tomada de decisão e crescimento sustentável.</span></p>
      <br>
      <hr>
      <br>
      <br>
      <h2><span style="color: #0354ea;">Quais os benefícios do CFO como um Serviço para meu negócio?</span></h2>
      <p><span style="color: rgb(255, 255, 255);">Mais controle, mais visão e mais resultados. Tenha relatórios inteligentes, previsibilidade de caixa e apoio na definição de metas financeiras.</span></p>
      <br>
      <hr>
      <br>
      <br>
      <h2><span style="color: #0354ea;">Que tipo de empresa pode contar com a Moura Costa?</span></h2>
      <p><span style="color: rgb(255, 255, 255);">Empresas em crescimento - principalmente pequenas e médias - que buscam mais organização, lucratividade e visão estratégica das finanças.</span></p>
      <br>
      <hr>
      <br>
      <br>
      <h2><span style="color: #0354ea;">Como posso solicitar uma proposta ou falar com a equipe?</span></h2>
      <p><span style="color: rgb(255, 255, 255);">É simples: preencha nosso formulário ou chame no WhatsApp. Nosso time responderá o mais rápido possível.</span></p>
      <br>
      <hr>
      <br>
      <a href="#shop" class="button button-consultor" style="margin-top: 24px;">Falar com consultor</a>
      <br>
    </div>
  </div>
</section>
    <!-- IMAGEM :: Justificar a imagem a esquerda-->

<!-- Justificar texto a esquerda-->


    <!-- Aqui você pode inserir o formulário futuramente -->
  </div>

</section>

<!-- Novo bloco com background de cadastro sem formulário de inscrição centralizado até o formulário de inscrição -->
<section class="escopo-flex" id="escopo" style="background: linear-gradient(90deg, #0354ea 0%, #040009 100%); color: #f0ebebc5; padding: 60px 40px;">
  <div class="escopo-texto_bloco_05">
    <h1 style="font-size: 32px; margin-bottom: 30px;">
    NOSSOS CLIENTES CONFIAM E INDICAM. </h1> <br>

<div class="carrossel-container">
  <div class="carrossel" id="carrossel">
    <div class="slide"><img src="Carro_01.png" alt="Logo 1" /></div>
    <div class="slide"><img src="Carro_02.png" alt="Logo 2" /></div>
    <div class="slide"><img src="Carro_03.png" alt="Logo 3" /></div>
    <div class="slide"><img src="Carro_04.png" alt="Logo 4" /></div>
    <div class="slide"><img src="Carro_05.png" alt="Logo 5" /></div>
  </div>
  <div class="dots" id="dots"></div>
</div>


<script>
  const carrossel = document.getElementById("carrossel");
  const slides = carrossel.children;
  const dotsContainer = document.getElementById("dots");
  const totalPages = Math.ceil(slides.length / 4);
  let currentPage = 0;

  // Criar bolinhas (páginas)
  for (let i = 0; i < totalPages; i++) {
    const dot = document.createElement("span");
    dot.addEventListener("click", () => goToSlide(i));
    if (i === 0) dot.classList.add("active");
    dotsContainer.appendChild(dot);
  }

  function goToSlide(index) {
    currentPage = index;
    const slideWidth = slides[0].offsetWidth + 20; // Slide + margem
    carrossel.style.transform = `translateX(-${slideWidth * 3 * index}px)`;

    document.querySelectorAll(".dots span").forEach(dot => dot.classList.remove("active"));
    dotsContainer.children[index].classList.add("active");
  }

  window.addEventListener("resize", () => goToSlide(currentPage));
</script>

<br>
<br>
    <h2 style="font-size: 20px; margin-bottom: 30px;">MUITAS ASSESORIAS PROMETEM O IMPOSSÍVEL, E O CLIENTE ACABA COM PREJUÍZO, <br> NA MOURA COSTA PRIORIZAMOS NOSSOS CLIENTES ACIMA DE TUDO, MANTENDO A PROXIMIDADE <br> E GARANTINDO A CONFIANÇA NO QUE FAZEMOS. </h2> 
    <br>
<a href="#shop" class="button button-consultor">Falar com consultor</a>

<!-- Texto Bloco 05 A ESQUERDA :: Faça seu orçamento-->
<!-- Preeencha o formulário e nossa equipe entrará em contato: botões: Nome completo, E-mail, Telefone; por fim: Enviar-->

    <!-- Aqui você pode inserir o formulário futuramente -->
  </div>

</section>

<!-- Texto Bloco 05 A ESQUERDA :: Faça seu orçamento-->
<!-- Preeencha o formulário e nossa equipe entrará em contato: botões: Nome completo, E-mail, Telefone; por fim: Enviar-->
<!-- Formulário-->

<!-- FORMULÁRIO E CONTATO -->
<section class="orcamento-contato">
  <div class="orcamento">
    <h2>Faça o seu orçamento </h2>
    <p><strong>Encontre soluções acessíveis e flexíveis para sua situação financeira com nossos serviços.</strong></p>
    <form>
      <p><strong>Preencha o formulário e nossa equipe entrará em contato:</strong></p>
      <input type="text" placeholder="Nome completo" required>
      <div class="input-duplo">
        <input type="email" placeholder="E-mail" required>
        <input type="tel" placeholder="Telefone" required>
      </div>
      <button type="submit" class="button-formulario">Enviar</button>
    </form>
  </div>


<!-- Texto Bloco 05 A DIREITA :: Fale conosco, adereços, ícones de: e-mail, e redes sociais-->

  <div class="contato">
    <h2>FALE CONOSCO</h2>
    <p><strong>21 973 575 543</strong></p>
    <p><strong>84 8132-3236</strong></p>
    <p class="email">comercial@mouracostafinanceiro.com.br</p>

    <div class="icones-contato">
      <img src="email-icon.png" alt="Email" />
      <img src="whatsapp-icon.png" alt="WhatsApp" />
    </div>

    <!-- NOVO BLOCO DE PERFIS -->
    <div class="contato-equipe">
        <div class="membro">
        <img src="rafael_moura_costa.jpeg" alt="Rafael Moura">
        <div class="texto">
            <p class="nome">Rafael Moura</p>
            <p class="cargo">CEO e Fundador</p>
            <p class="empresa">Moura Costa assessoria<br>Financeira Empresarial</p>
        </div>
        </div>
        <div class="membro">
        <img src="dutra.png" alt="Vitor Dultra">
        <div class="texto">
            <p class="nome">Vitor Dultra</p>
            <p class="cargo">Consultor de Finanças<br><span class="junior">Junior</span></p>
        </div>
        </div>
    </div>


    <p class="redes-title">Siga nossas rede sociais</p>
    <div class="redes">
      <img src="facebook-icon.png" alt="Facebook" />
      <img src="linkedin-icon.png" alt="LinkedIn" />
      <img src="instagram-icon.png" alt="Instagram" />
    </div>
  </div>
</section>

<!-- Justificar texto a esquerda-->


    <!-- Aqui você pode inserir o formulário futuramente -->
  </div>

</section>


<section class="bloco-imagem">
  <img src="site_home_antes_rodape.png" alt="Descrição da imagem" />
</section>


<!-- Rodapé - Bloco  dividido por 3 colunas -->

<section class="footer_02"> 

    <footer class="footer_01">
    <!-- Coluna 1: Logo -->
    <div class="footer-column footer-logo">
    <img src="Ativo_rodape_branco.png" alt="Logo Moura Costa" class="footer-logo-img">
      <small>MOURA COSTA ASSESSORIA FINANCEIRA LTDA<br>CNPJ: 55.709.917/0001-512</small>
    </div>

<!-- Coluna 2: Serviços -->
    <div class="footer-column footer-services">
      <h3>NOSSOS SERVIÇOS</h3>
      <br>
      <br>

      <ul>
        <li>Recursos Humanos</li>
        <li>Departamento Pessoal</li>
        <li>BPO Financeiro</li>
        <li>Gestão de Processos</li>
      </ul>
    </div>

<!-- Coluna 3: Contato e Redes Sociais -->

  <div class="footer-column footer-contact">
      <div class="social-icons">
        <a href="#"><!-- Facebook -->
          <i class="fab fa-facebook-f">f</i>
        </a>
        <a href="#"><!-- LinkedIn -->
          <i class="fab fa-linkedin-in">in</i>
        </a>
        <a href="#"><!-- Instagram -->
          <i class="fab fa-instagram">📷</i>
        </a>
        <a href="#"><!-- WhatsApp -->
          <i class="fab fa-whatsapp">🟢</i>
        </a>
      </div>
      <p>21 973 575 543 📱</p>
      <p>84 8132-3236</p>
      <p><a href="mailto:comercial@mouracostafinanceiro.com.br">COMERCIAL@MOURACOSTAFINANCEIRO.COM.BR</a></p>
    </div>




</section>

<footer class="footer">
  <div class="footer-content">
    <div class="footer-text">
      <p class="footer-p-grande">&copy; MOURA COSTA ASSESSORIA FINANCEIRA LTDA. <br>
      <br>
      <p class="footer-p-pequeno">UTILIZAMOS COOKIES ESSENCIAIS E TECNOLOGIAS SEMELHANTES DE ACORDO COM A POLÍTICA DE PRIVACIDADE, E AO CONTINUAR NAVEGANDO, VOCÊ CONCORDA COM ESTAS CONDIÇÕES. SAIBA MAIS.</p>
    </div>
  </div>
</footer>

</body>
</html>
