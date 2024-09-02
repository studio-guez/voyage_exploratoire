<template>
    <footer class="v-app-footer app-child-rm-horizontal-margins"
    >
      <p>S'abonner à la newsletter :</p>
      <input type="text" placeholder="adresse mail"/>

      <div v-html='`
      <form method="post" action="https://newsletter.infomaniak.com/v3/api/1/newsletters/webforms/18211/submit" class="inf-form"><input type="email" name="email" style="display:none" /><input type="hidden" name="key" value="eyJpdiI6IkxQcUNoYVdFUE9KM0dPbGgxa1lMazVUTjZNOGtoUkJmbmdCWTRFZ0kyclk9IiwibWFjIjoiMmZkYTYwODAyYjAyYmU5ODczOGJlODExNjlkOTgwYTM2ZmY2NjgzMjVhYTU4OTEyMWZlM2M4OTI3NzM1MzU2MiIsInZhbHVlIjoiVzVDbDVCWXN4M0U3a0VIT3dEMVZwTEt3QlFaNXVlaG9LUTFRRDA3bXlXMD0ifQ=="><input type="hidden" name="webform_id" value="18211">
            <style>
                .inf-main_4186b8943907012bd947930996fe9051{
                background-color:#f5f5f5;
                padding:25px 20px;
                margin:25px auto;
                }
                .inf-main_4186b8943907012bd947930996fe9051 .inf-content {
                margin-top:13px;
                } .inf-main_4186b8943907012bd947930996fe9051 h4, .inf-main_4186b8943907012bd947930996fe9051 span, .inf-main_4186b8943907012bd947930996fe9051 label, .inf-main_4186b8943907012bd947930996fe9051 input, .inf-main_4186b8943907012bd947930996fe9051 .inf-submit, .inf-main_4186b8943907012bd947930996fe9051 .inf-success p a { color:#555555; font-size:14px; } .inf-main_4186b8943907012bd947930996fe9051 h4{ font-size:18px; margin:0px 0px 13px 0px; } .inf-main_4186b8943907012bd947930996fe9051 h4, .inf-main_4186b8943907012bd947930996fe9051 label{ font-weight:bold; } .inf-main_4186b8943907012bd947930996fe9051 .inf-input { margin-bottom:7px; } .inf-main_4186b8943907012bd947930996fe9051 label { display:block;} .inf-main_4186b8943907012bd947930996fe9051 input{ height:35px; color:#999999; border: 1px solid #E9E9E9; border:none; padding-left:7px; } .inf-main_4186b8943907012bd947930996fe9051 .inf-input.inf-error label, .inf-main_4186b8943907012bd947930996fe9051 .inf-input.inf-error span.inf-message{ color: #cc0033; } .inf-main_4186b8943907012bd947930996fe9051 .inf-input.inf-error input{ border: 1px solid #cc0033; } .inf-main_4186b8943907012bd947930996fe9051 .inf-input input { width:100%;} .inf-main_4186b8943907012bd947930996fe9051 .inf-input.inf-error span.inf-message { display: block; } .inf-main_4186b8943907012bd947930996fe9051 .inf-submit { text-align:right;} .inf-main_4186b8943907012bd947930996fe9051 .inf-submit input{ background-color:#777777; color:#ffffff; border:none; font-weight: normal; height:auto; padding:7px; } .inf-main_4186b8943907012bd947930996fe9051 .inf-submit input.disabled{ opacity: 0.4; } .inf-btn { color: rgb(85, 85, 85); border: medium none; font-weight: normal; height: auto; padding: 7px; display: inline-block; background-color: white; box-shadow: 0px 1px 1px rgba(0, 0, 0, 0.24); border-radius: 2px; line-height: 1em; } .inf-rgpd { margin:25px 0px 15px 0px; color:#555555; } </style><div class="inf-main_4186b8943907012bd947930996fe9051"> <h4></h4> <span></span> <div class="inf-success" style="display:none"> <h4>Votre inscription a été enregistrée avec succès !</h4> <p> <a href="#" class="inf-btn">&laquo;</a> </p> </div> <div class="inf-content"> <div class="inf-input inf-input-text"> <input type="email" name="inf[1]" data-inf-meta="1" data-inf-error="" required="required" placeholder="Email *" > </div> <div class="inf-rgpd">Votre adresse de messagerie est uniquement utilisée pour vous envoyer notre lettre d&#039;information ainsi que des informations concernant nos activités. Vous pouvez à tout moment utiliser le lien de désabonnement intégré dans chacun de nos mails.</div> <div style=""> <label data-mcaptcha_url="https://captcha.infomaniak.com/widget/?sitekey=wKJaAigS1e48fWgqtjvg5w7rKA6QIwmy" for="mcaptcha__token" id="mcaptcha__token-label"> <input type="text" name="mcaptcha__token" id="mcaptcha__token"/> </label> <div id="mcaptcha__widget-container"></div> <script src="https://unpkg.com/@mcaptcha/vanilla-glue@0.1.0-rc2/dist/index.js"></script> </div> <div class="inf-submit"> <input type="submit" style="margin-top: 25px;" name="" value="Envoyé"> </div> </div> </div> </form>
      `'/>

      <p>Nous contacter :
        <br>super@lesfantastiquescommuns.cc
        <br>
        <br>L'association les fantastiques communs
        <br>route de la Galaise 23A, 1228 Plan-les-Ouates
      </p>
    </footer>
</template>





<script setup lang="ts">
import { defineProps } from 'vue'

const props = defineProps<{
    message?: string
}>()
</script>





<style lang="scss" scoped >
.v-app-footer {
  box-sizing: border-box;
  padding: var(--app-gutter);
  color: white;
  background: var(--app-color-beige--dark);
}

input {
  background: transparent;
  border: solid 1px currentColor;
  color: inherit;
  display: block;
  box-sizing: border-box;
  font-size: .75rem;
  line-height: 1.25em;
  padding: 1em;
  width: 100%;
  border-radius: 2em;

  &::placeholder {
    color: inherit;
    text-transform: uppercase;
  }
}

</style>
