---
layout: post
title: 'chkdsk x: /f /r'
date: 2026-01-12 12:02:48 +00:00
---

<p class="wp-block-paragraph">O comando <code>chkdsk</code> (abreviação de <strong>Check Disk</strong>) é uma das ferramentas de manutenção mais poderosas e antigas do Windows. Ele serve para examinar a integridade física e lógica do seu disco rígido (HD) ou SSD.</p>



<p class="wp-block-paragraph">Aqui está o que cada parte desse comando específico faz:</p>



<h3 class="wp-block-heading">A Anatomia do Comando</h3>



<ul class="wp-block-list">
<li><strong><code>chkdsk</code></strong>: Chama o programa de verificação de disco.</li>



<li><strong><code>x:</code></strong>: É a letra da unidade que você quer verificar (você deve substituir o <strong>x</strong> pela letra real, como <code>c:</code>, <code>d:</code> ou <code>e:</code>).</li>



<li><strong><code>/f</code></strong>: (Fix) Corrige erros encontrados no sistema de arquivos (erros de software).</li>



<li><strong><code>/r</code></strong>: (Recover) Localiza setores defeituosos (<strong>bad sectors</strong>) no disco físico e tenta recuperar qualquer informação legível neles.</li>
</ul>



<blockquote class="wp-block-quote is-layout-flow wp-block-quote-is-layout-flow">
<p class="wp-block-paragraph"><strong>Nota importante:</strong> O parâmetro <code>/r</code> já inclui tudo o que o <code>/f</code> faz, mas de uma forma muito mais profunda e lenta.</p>
</blockquote>



<hr class="wp-block-separator has-alpha-channel-opacity" />



<h3 class="wp-block-heading">O que ele faz na prática?</h3>



<figure class="wp-block-table"><table class="has-fixed-layout"><thead><tr><td><strong>Fase</strong></td><td><strong>O que acontece</strong></td></tr></thead><tbody><tr><td><strong>Correção Lógica</strong></td><td>Ele organiza o &#8220;índice&#8221; do Windows. Se o sistema diz que um arquivo está em um lugar, mas ele não está, o <code>chkdsk /f</code> limpa essa bagunça.</td></tr><tr><td><strong>Verificação Física</strong></td><td>Com o <code>/r</code>, ele testa a superfície física do disco. Se ele encontra um pedaço do HD que está &#8220;morrendo&#8221;, ele marca aquele ponto como inutilizável para que o Windows não salve nada lá e cause travamentos.</td></tr></tbody></table></figure>



<hr class="wp-block-separator has-alpha-channel-opacity" />



<h3 class="wp-block-heading">Quando usar este comando?</h3>



<ul class="wp-block-list">
<li>Se o computador está dando <strong>Tela Azul</strong> com frequência.</li>



<li>Se o Windows está muito lento para abrir pastas ou salvar arquivos.</li>



<li>Se você suspeita que seu HD/SSD antigo está começando a falhar fisicamente.</li>



<li>Se o Windows notificou que &#8220;encontrou erros na unidade&#8221;.</li>
</ul>



<h3 class="wp-block-heading">⚠️ Avisos Importantes:</h3>



<ol start="1" class="wp-block-list">
<li><strong>Demora muito:</strong> Dependendo do tamanho do seu disco e da quantidade de erros, o processo com <code>/r</code> pode levar de <strong>30 minutos a várias horas</strong>. Não interrompa o processo.</li>



<li><strong>Uso do Disco:</strong> Se você tentar rodar no <code>C:</code> (onde o Windows está instalado), ele dirá que não pode bloquear a unidade e perguntará se você deseja agendar a verificação para a próxima vez que o computador reiniciar. Digite <strong>S</strong> (ou <strong>Y</strong>) e reinicie.</li>



<li><strong>SSD vs HD:</strong> Em SSDs modernos, o <code>/r</code> é menos necessário que em HDs mecânicos, mas ainda útil para encontrar células de memória corrompidas.</li>
</ol>



<p class="wp-block-paragraph"></p>

<!-- Fonte original: https://marcuspavan.wordpress.com/2026/01/12/chkdsk-x-f-r/ -->
