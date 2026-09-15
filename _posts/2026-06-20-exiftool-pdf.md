---
layout: post
title: 'ExifTool PDF'
date: 2026-06-20 18:16:26 +00:00
---

<p class="wp-block-paragraph">O&nbsp;<strong>ExifTool&nbsp;</strong>é um software&nbsp;<strong>gratuito e de código aberto</strong>&nbsp;(Open Source), desenvolvido por Phil Harvey.</p>



<p class="wp-block-paragraph">Você pode usá-lo livremente tanto para fins pessoais quanto&nbsp;<strong>comerciais</strong>&nbsp;sem pagar licenças. Ele é distribuído sob os mesmos termos do próprio Perl (geralmente sob a&nbsp;<em>GPL</em>&nbsp;ou a&nbsp;<em>Artistic License</em>), o que significa que ele é extremamente permissivo.</p>



<h3 class="wp-block-heading">Por que ele é tão usado em empresas e no governo?</h3>



<ol start="1" class="wp-block-list">
<li><strong>Custo Zero:</strong> Não há taxas de assinatura ou compra.</li>



<li><strong>Segurança:</strong> Por ser offline e via linha de comando, ele não envia seus documentos para servidores externos (diferente de sites que prometem “editar metadados online”).</li>



<li><strong>Automação:</strong> Como funciona via prompt, você pode criar um arquivo <code>.bat</code> ou um script em Python para processar milhares de PDFs de uma vez só, aplicando os metadados exigidos por lei automaticamente.</li>
</ol>



<hr class="wp-block-separator has-alpha-channel-opacity" />



<h3 class="wp-block-heading">Exemplo Prático: Comando para conformidade legal (Decreto 10.278)</h3>



<p class="wp-block-paragraph">Se você precisar adequar um arquivo PDF aos requisitos brasileiros de digitalização, o comando no ExifTool seria algo parecido com isto:</p>



<p class="wp-block-paragraph">Bash</p>


<div class="wp-block-code">
	<div class="cm-editor">
		<div class="cm-scroller">
			
<pre>
<code><div class="cm-line">exiftool -overwrite_original ^-Title=&quot;Contrato de Servico 001&quot; ^-Author=&quot;Sua Empresa LTDA&quot; ^-Subject=&quot;Documento Digitalizado conforme Decreto 10.278/2020&quot; ^-Creator=&quot;Responsavel pela Digitalizacao&quot; ^-Description=&quot;Digitalizado em 22/01/2026 em Londrina-PR&quot; ^-Keywords=&quot;Juridico, Contratos, 2026&quot; ^documento.pdf</div></code></pre>
		</div>
	</div>
</div>


<h3 class="wp-block-heading">Onde baixar?</h3>



<p class="wp-block-paragraph">O site oficial é o&nbsp;<a target="_blank" rel="noopener" href="https://exiftool.org/">exiftool.org</a>. No Windows, você baixa um arquivo&nbsp;<code>.zip</code>, extrai o&nbsp;<code>exiftool(-k).exe</code>, renomeia para apenas&nbsp;<code>exiftool.exe</code>&nbsp;e já pode usar via CMD ou PowerShell.</p>



<p class="wp-block-paragraph"><a target="_blank" rel="noopener" href="https://www.youtube.com/watch?v=6JDy3UUkiB8">Aprenda a instalar e usar o ExifTool no Windows</a></p>

<!-- Fonte original: https://marcuspavan.wordpress.com/2026/06/20/exiftool-pdf/ -->
