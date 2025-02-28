<template>
    <footer class="v-app-footer app-child-rm-horizontal-margins"
    >
      <p>S'abonner à la newsletter :</p>

      <form method="post"
            action="https://newsletter.infomaniak.com/v3/api/1/newsletters/webforms/18211/submit"
            class="inf-form">
        <input type="email" name="email" style="display:none"/>
        <input type="hidden" name="key"
               value="eyJpdiI6ImRuVGpEVEpRSGFqTFNXSGFDRk5CQks4XC9PSkhSb2pxc1UxYzlLTmFvTFR3PSIsIm1hYyI6ImVhOTgzNDIxZjhhMmU3OTBiNWVhYzcwOTFkN2Y1OTU3MWNmMjZjODkzZDljZTU1MjQ3YzE3ZWU4NWVhMDljMTYiLCJ2YWx1ZSI6IllzQjZjU2hxSzJtWVo3RE9NTWpiRXhqcTBBOWZRYnRNdmpTOG5RYmFNM289In0=">
        <input type="hidden" name="webform_id" value="18211">
        <div class="inf-main_4186b8943907012bd947930996fe9051"><h4></h4> <span></span>
          <div class="inf-success" style="display:none"><h4>Votre inscription a été enregistrée avec succès !</h4>
            <p><a href="#" class="inf-btn">&laquo;</a></p></div>
          <div class="inf-content">
            <div class="inf-input inf-input-text"><input type="email" name="inf[1]" data-inf-meta="1" data-inf-error=""
                                                         required="required" placeholder="Email *"></div>
            <div class="recaptcha-container"><label
                    data-mcaptcha_url="https://captcha.infomaniak.com/widget/?sitekey=wKJaAigS1e48fWgqtjvg5w7rKA6QIwmy"
                    for="mcaptcha__token" id="mcaptcha__token-label"> <input type="text" name="mcaptcha__token"
                                                                             id="mcaptcha__token"/> </label>
              <div id="mcaptcha__widget-container"></div>
              <component is="script" src="https://unpkg.com/@mcaptcha/vanilla-glue@0.1.0-rc2/dist/index.js"></component>
            </div>
            <div class="inf-submit"><input type="submit" style="margin-top: 25px;" name="" value="Envoyé"></div>
          </div>
        </div>
      </form>

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
#mcaptcha__widget-container {
  width: calc(100% + 10rem);
  height: 100%;
}

.inf-content {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  justify-content: center;
  gap: 1rem 5rem;
}

.inf-input.inf-input-text {
  width: 100%;
}

.inf-submit {
  width: 10rem;
}

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

.recaptcha-container {
  overflow: hidden;
  width: 16rem;
  background: #ffffff;
  border-radius: 5rem;
  height: 2.5rem;
  padding-left: 4.5rem;

  iframe {

  }
}

</style>
