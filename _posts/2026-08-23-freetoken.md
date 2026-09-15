---
layout: post
title: 'FreeToken'
date: 2026-08-23 17:08:40 +00:00
---

<figure class="wp-block-image size-large"><a href="https://marcuspavan.wordpress.com/wp-content/uploads/2026/08/image-2.png"><img loading="lazy" width="1024" height="211" data-attachment-id="336" data-permalink="https://marcuspavan.wordpress.com/2026/08/23/freetoken/image-17/" data-orig-file="https://marcuspavan.wordpress.com/wp-content/uploads/2026/08/image-2.png" data-orig-size="1048,216" data-comments-opened="1" data-image-meta="{&quot;aperture&quot;:&quot;0&quot;,&quot;credit&quot;:&quot;&quot;,&quot;camera&quot;:&quot;&quot;,&quot;caption&quot;:&quot;&quot;,&quot;created_timestamp&quot;:&quot;0&quot;,&quot;copyright&quot;:&quot;&quot;,&quot;focal_length&quot;:&quot;0&quot;,&quot;iso&quot;:&quot;0&quot;,&quot;shutter_speed&quot;:&quot;0&quot;,&quot;title&quot;:&quot;&quot;,&quot;orientation&quot;:&quot;0&quot;,&quot;alt&quot;:&quot;&quot;}" data-image-title="image" data-image-description="" data-image-caption="" data-large-file="https://marcuspavan.wordpress.com/wp-content/uploads/2026/08/image-2.png?w=1024" src="https://marcuspavan.wordpress.com/wp-content/uploads/2026/08/image-2.png?w=1024" alt="" class="wp-image-336" srcset="https://marcuspavan.wordpress.com/wp-content/uploads/2026/08/image-2.png?w=1024 1024w, https://marcuspavan.wordpress.com/wp-content/uploads/2026/08/image-2.png?w=150 150w, https://marcuspavan.wordpress.com/wp-content/uploads/2026/08/image-2.png?w=300 300w, https://marcuspavan.wordpress.com/wp-content/uploads/2026/08/image-2.png?w=768 768w, https://marcuspavan.wordpress.com/wp-content/uploads/2026/08/image-2.png 1048w" sizes="auto, (max-width: 1024px) 100vw, 1024px" /></a></figure>



<p class="wp-block-paragraph">O repositório <strong>FreeToken</strong> (<code>[https://github.com/FlashML-org/FreeToken](https://github.com/FlashML-org/FreeToken)</code>), desenvolvido pela organização <strong>FlashML</strong> (com pesquisadores de instituições como UC Berkeley e UT Austin), é um motor de inferência e servidor de código aberto (<em>edge-native serving engine</em>) focado em <strong>executar modelos de linguagem gigantescos baseados em arquitetura Mixture of Experts (MoE) em hardware comum/de consumidor</strong>.</p>



<h3 class="wp-block-heading">💡 Qual é o objetivo do projeto?</h3>



<p class="wp-block-paragraph">Modelos avançados com centenas de bilhões de parâmetros (como Qwen, GLM, DeepSeek e Kimi) normalmente exigem clusters de GPUs de centros de dados extremamente caros para rodar.<sup></sup></p>



<p class="wp-block-paragraph">O <strong>FreeToken</strong> resolve esse gargalo ao transformar o computador pessoal (seja um laptop ou desktop de alta performance) em uma plataforma unificada de inferência.<sup></sup>Ele combina a memória da GPU, o processador (CPU), a memória RAM e o barramento PCIe para otimizar o fluxo de dados em tempo real.<sup></sup></p>



<h3 class="wp-block-heading">🛠️ Como ele funciona? (Principais Inovações)</h3>



<ol start="1" class="wp-block-list">
<li><strong>Execução Adaptativa de Banda (Bandwidth-Adaptive Execution):</strong>Em modelos MoE, cada token aciona apenas uma fração de todos os especialistas (<em>experts</em>) do modelo.O FreeToken divide de forma inteligente o cálculo entre a GPU e a CPU/RAM, transferindo pesos via PCIe sem deixar a GPU ociosa.</li>



<li><strong>Caching Semântico e Estratégias de Cache de Especialistas:</strong>Mantém na GPU os especialistas mais requisitados utilizando estratégias de substituição inteligente de cache, reduzindo drasticamente a transferência desnecessária de dados.</li>



<li><strong>Double Buffering no Prefill:</strong>Sobrepõe o carregamento da próxima camada via PCIe enquanto a camada atual é processada pela GPU, garantindo altíssima velocidade de geração de texto.</li>
</ol>



<h3 class="wp-block-heading">📊 Desempenho e Recursos</h3>



<ul class="wp-block-list">
<li><strong>Grandes Modelos em GPUs Únicas:</strong>Permite rodar modelos MoE de grande escala (como modelos de 35B a 284B e até mesmo o GLM-5.2 de 753B) em uma única GPU de estação de trabalho ou desktop gamer combinada com bastante RAM no sistema.</li>



<li><strong>API Compatível:</strong>Possui suporte a endpoints compatíveis com as APIs da OpenAI e Anthropic (porta padrão <code>1919</code>), facilitando a integração com assistentes de código como Claude Code, Codex e agentes de IA locais.</li>



<li><strong>Licença:</strong>Código sob licença aberta Apache-2.0.</li>
</ul>

<!-- Fonte original: https://marcuspavan.wordpress.com/2026/08/23/freetoken/ -->
