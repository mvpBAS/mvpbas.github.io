---
layout: post
title: 'pendrive bootável / gravar em ntfs'
date: 2026-05-13 19:21:12 +00:00
---

<p class="wp-block-paragraph">Sim, você consegue fazer isso sem problemas. A maioria das distribuições Linux modernas já vem com suporte nativo a <strong>NTFS</strong> através do driver <strong>ntfs-3g</strong>, permitindo montar e acessar partições do Windows (como o drive C:) diretamente pelo pendrive bootável.</p>



<h3 class="wp-block-heading">Como criar o pendrive bootável</h3>



<ol class="wp-block-list">
<li><strong>Escolher a distribuição</strong>
<ul class="wp-block-list">
<li><strong>Ubuntu</strong> ou <strong>Linux Mint</strong>: fáceis de usar, com suporte NTFS pronto.</li>



<li><strong>SystemRescue</strong>: voltada para manutenção e recuperação de sistemas, ótima para esse tipo de tarefa.</li>



<li><strong>Hiren’s BootCD PE</strong> (embora seja baseado em Windows, também funciona bem para acesso NTFS).</li>
</ul>
</li>



<li><strong>Criar o pendrive</strong>
<ul class="wp-block-list">
<li>No Windows, use programas como <strong>Rufus</strong> ou <strong>balenaEtcher</strong>.</li>



<li>No Linux, pode usar o comando <code>dd</code> ou o <strong>Ventoy</strong> (que permite colocar várias ISOs no mesmo pendrive).</li>
</ul>
</li>



<li><strong>Dar boot pela USB</strong>
<ul class="wp-block-list">
<li>Entre na BIOS/UEFI da máquina e configure para iniciar pelo pendrive.</li>



<li>Carregue o Linux em modo “Live”.</li>
</ul>
</li>



<li><strong>Montar a partição NTFS</strong>
<ul class="wp-block-list">
<li>Normalmente o sistema já detecta e monta automaticamente.</li>



<li>Se precisar montar manualmente: 
<ul class="wp-block-list">
<li><code>sudo mkdir /mnt/c </code></li>



<li><code>sudo mount -t ntfs-3g /dev/sda1 /mnt/c</code> <em>(substitua <code>/dev/sda1</code> pelo identificador correto da partição C:)</em></li>



<li>fdisk -l (lista as partições)</li>
</ul>
</li>
</ul>
</li>



<li><strong>Remover a pasta</strong>
<ul class="wp-block-list">
<li>Depois de montada, basta navegar até <code>/mnt/c</code> e apagar a pasta com <code>rm -rf nome_da_pasta</code>.</li>
</ul>
</li>
</ol>



<hr class="wp-block-separator has-alpha-channel-opacity" />



<p class="wp-block-paragraph">👉 Se quiser algo bem direto e leve, eu recomendaria o <strong>SystemRescue</strong>: ele já vem com ferramentas para manipular NTFS e é feito justamente para manutenção.</p>



<p class="wp-block-paragraph"><strong>O programa mais recomendado para criar um pendrive bootável com o SystemRescue é o <em>Rufus</em>, por ser leve, rápido e compatível com praticamente qualquer ISO. Alternativamente, você pode usar o <em>balenaEtcher</em> (mais simples e multiplataforma) ou o <em>Ventoy</em> (permite colocar várias ISOs no mesmo pendrive).</strong> <a href="https://www.system-rescue.org/">System Rescue</a> <a href="https://sourceforge.net/projects/systemrescuecd/">SourceForge</a></p>



<hr class="wp-block-separator has-alpha-channel-opacity" />



<h2 class="wp-block-heading">🔧 Programas recomendados para criar pendrive bootável</h2>



<figure class="wp-block-table"><table class="has-fixed-layout"><thead><tr><th><strong>Rufus</strong></th><th><strong>balenaEtcher</strong></th><th><strong>Ventoy</strong></th></tr></thead><tbody><tr><td>Mais popular no Windows</td><td>Multiplataforma (Windows, Linux, macOS)</td><td>Permite múltiplas ISOs no mesmo pendrive</td></tr><tr><td>Interface simples, várias opções de formatação</td><td>Interface extremamente simples (arrastar e soltar)</td><td>Ideal para quem quer ter várias ferramentas no mesmo USB</td></tr><tr><td>Suporte a BIOS e UEFI</td><td>Suporte a BIOS e UEFI</td><td>Suporte a BIOS e UEFI</td></tr><tr><td>Recomendado para uso direto com SystemRescue</td><td>Ótimo para iniciantes</td><td>Ótimo para técnicos e manutenção</td></tr></tbody></table></figure>



<hr class="wp-block-separator has-alpha-channel-opacity" />



<h2 class="wp-block-heading">🚀 Passo a passo com Rufus</h2>



<ol class="wp-block-list">
<li>Baixe e instale o <strong>Rufus</strong>.</li>



<li>Insira o pendrive (mínimo 2 GB).</li>



<li>Selecione a ISO do <strong>SystemRescue</strong>.</li>



<li>Configure:
<ul class="wp-block-list">
<li><strong>Partição GPT</strong> se for UEFI, ou <strong>MBR</strong> se for BIOS legado.</li>



<li>Sistema de arquivos: <strong>FAT32</strong> (mais compatível).</li>
</ul>
</li>



<li>Clique em <strong>Iniciar</strong> e aguarde a gravação.</li>
</ol>



<hr class="wp-block-separator has-alpha-channel-opacity" />



<h2 class="wp-block-heading">⚠️ Pontos importantes</h2>



<ul class="wp-block-list">
<li><strong>Backup do pendrive</strong>: o processo apaga todos os dados.</li>



<li><strong>Compatibilidade</strong>: se a máquina for antiga, prefira MBR; se for moderna, GPT/UEFI.</li>



<li><strong>Montagem NTFS</strong>: o SystemRescue já vem com suporte completo ao NTFS via <code>ntfs-3g</code>.</li>
</ul>



<hr class="wp-block-separator has-alpha-channel-opacity" />



<p class="wp-block-paragraph">👉 Se você quer algo rápido e direto, vá de <strong>Rufus</strong>. Se prefere simplicidade extrema, use <strong>balenaEtcher</strong>. Se quiser montar um pendrive “canivete suíço” com várias ISOs (SystemRescue, Ubuntu Live, etc.), escolha <strong>Ventoy</strong>.</p>



<p class="wp-block-paragraph">Quer que eu detalhe o <strong>passo a passo com Ventoy</strong> para você poder colocar o SystemRescue junto com outras ISOs no mesmo pendrive?</p>

<!-- Fonte original: https://marcuspavan.wordpress.com/2026/05/13/pendrive-bootavel-gravar-em-ntfs/ -->
