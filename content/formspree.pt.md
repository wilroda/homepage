+++
weight = 60
menuname = "Contactos"
draft = false
+++

<form id="contactform" method="post" action="https://formspree.io/gamejamneuro@gmail.com">
	<div class="field half first">
		<input type="text" name="name" id="name" placeholder="Nome"/>
	</div>
	<div class="field half">
		<input type="email" id="email" name="email" placeholder="Email">
	</div>
	<div class="field">
		<textarea name="message" id="message" rows="4" placeholder="Mensagem"></textarea>
	</div>
	<ul class="actions">
		<li><input type="submit" value="Enviar" class="special" /></li>
		<li><input type="reset" value="Cancelar" /></li>
	</ul>
	<input type="hidden" name="_next" value="?sent#formspree" />
	<input type="hidden" name="_subject" value="Website form message" />
	<input type="text" name="_gotcha" style="display:none" />
</form>
<span id="contactformsent">Obrigado pelo contacto!</span>

<script>
$(document).ready(function($) {
    $(function(){
        if (window.location.search == "?sent") {
        	$('#contactform').hide();
        	$('#contactformsent').show();
        } else {
        	$('#contactformsent').hide();
        }
    });
});
</script>


{{< socialLinks >}}
