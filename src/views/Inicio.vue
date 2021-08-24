<template lang="pug">
section
  .banner-principal.mb-5
    .container.tarjeta.p-4.p-sm-5(
      :style="{'background-image': `url(${require('@/assets/curso/fondo-banner-principal.svg')})`}"
    )
      .row.justify-content-around.align-items-center
        .col-lg-7.col-xxl-6.banner-principal__info
          .banner-principal__programa
            .h1.mb-0 Venta consultiva de productos financieros
          
          .h2 Información del programa
          .banner-principal__datos
            ul
              li.mb-3.banner-principal__datos__item
                p.h6.mb-0.me-3.banner-principal__datos__item__titulo Nombre del programa: 
                p.banner-principal__datos__item__texto Venta consultiva de productos financieros
              li.mb-3.banner-principal__datos__item
                p.h6.mb-0.me-3.banner-principal__datos__item__titulo Código: 
                p.banner-principal__datos__item__texto 11120000
              li.mb-3.banner-principal__datos__item
                p.h6.mb-0.me-3.banner-principal__datos__item__titulo Total Horas: 
                p.banner-principal__datos__item__texto 48 Horas
              li.mb-3.banner-principal__datos__item
                p.h6.mb-0.me-3.banner-principal__datos__item__titulo Duración en semanas: 
                p.banner-principal__datos__item__texto 4 Semanas
              li.mb-3.banner-principal__datos__item
                p.h6.mb-0.me-3.banner-principal__datos__item__titulo Modalidad: 
                p.banner-principal__datos__item__texto virtual

        .d-none.d-lg-block.col-lg-5
          //- img(src="@/assets/curso/banner-princiapal.svg")
          .video
            | <iframe data-v-1f9e4816="" width="560" height="315" src="https://www.youtube.com/embed/2L91WMqw96A" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen="allowfullscreen"></iframe>

  .container.tarjeta.tarjeta__template--azul-claro.p-4.p-md-5.mb-5(data-aos="fade-up")
    .titulo__template--a.mb-4
      span.h4 1. Presentación

    p En este programa, se capacitará con el objetivo de poder conocer, aprender y diferenciar la forma de realizar una venta consultiva para productos financieros, que le permita entender el contexto de este sector, como lo son: los bancos, corredores de bolsa, fondos de pensiones y de cesantías, aseguradoras, entre otras. 
    
    p.mt-4 Reconocerá las formas de manejar fundamentos como: la venta consultiva, mercadeo digital, el e-commerce y medios de comercialización para la forma de interacción con el medio comercial.

    p.mt-4 Logrará su proyecto de vida generando estrategias significativas para realizar cierres de ventas exitosos.

  .container.tarjeta.tarjeta__template--azul-claro.p-4.p-md-5.mb-5(data-aos="fade-up")
    .titulo__template--a.mb-4
      span.h4 2. Justificación<br>del programa

    p Este programa tiene como objetivo capacitar y reforzar los conocimientos y habilidades de todas aquellas personas que trabajan o desean trabajar en el frente comercial de diferentes clases de compañías del sector financiero, como son bancos, corredores de bolsa, fondos de pensión e inversión, aseguradoras, entre otras. Se ha de tener presente que al ser un producto intangible lo que se comercializa, se requiere de cierta clase de factores y estrategias para lograr la confianza del prospecto cliente, tanto para realizar la primera venta como para generar una relación a largo plazo con él. En este sentido, la filosofía de trabajo que propone la teoría de la venta consultiva es el método que más se ajusta al logro de los objetivos comerciales de la empresa.

    p.mt-4 En esta formación se propone que el vendedor adopte el rol de consultor para el cliente potencial, por lo cual debe ser un experto en los productos que comercializa, conoce el perfil de cada prospecto e indaga en sus necesidades específicas.

  .container.tarjeta.tarjeta__template--azul-claro.p-4.p-md-5.mb-5(data-aos="fade-up")
    .titulo__template--a.mb-4
      span.h4 3. Competencia a <br>desarrollar

    ul(style="list-style:disc;padding:revert;")
      li Negociar productos o servicios de acuerdo con objetivos estratégicos.

  .container.tarjeta.tarjeta__template--azul-claro.p-4.p-md-5.mb-5(data-aos="fade-up")
    .titulo__template--a.mb-4
      span.h4 4. Perfil de<br>ingreso

    ul(style="list-style:disc;padding:revert;")
      li Carta de presentación expedida por la comunidad. 
      li Cumplir con el trámite de selección definido por el Centro.

  .container.tarjeta.tarjeta__template--azul-claro.p-4.p-md-5.mb-5(data-aos="fade-up")
    .titulo__template--a.mb-4
      span.h4 5. Estrategia metodológica

    p Centrada en la construcción de autonomía para garantizar la calidad de la formación en el marco de la formación por competencias, el aprendizaje por proyectos y el uso de técnicas didácticas activas que estimulan el pensamiento para la resolución de problemas simulados y reales; soportada en la utilización de las tecnologías de la información y la comunicación, integradas en ambientes abiertos y pluritecnológicos, que en todo caso recrean el contexto productivo y vinculan al aprendiz con la realidad cotidiana y el desarrollo de las competencias.

    p.mt-4 Igualmente, debe estimular de manera permanente la autocrítica y la reflexión del aprendiz sobre el quehacer y los resultados de aprendizaje que logra a través de la vinculación activa de las cuatro fuentes de información para la construcción de conocimiento:

    ul.mt-5(style="list-style:disc;padding:revert;")
      li El instructor - tutor
      li El entorno
      li Las TIC
      li El trabajo colaborativo

  //- Créditos
  .container.tarjeta.tarjeta__template--azul-claro.p-4.p-md-5.mb-5(data-aos="fade-up")
    .titulo__template--a.mb-4
      span.h4 Créditos

    
    .creditos
      div(
        v-for="(creditoKey, index) of Object.keys(creditosData)"
        :class="index != Object.keys(creditosData).length -1 ? 'mb-4' : ''" 
      )
        .creditos__titulo {{configTitulos[creditoKey]}}
        table
          tbody
            tr(
              v-for="(item, idx) of creditosData[creditoKey]" 
              :key="creditoKey+idx"
            )
              td.text-bold(colspan='2' v-html="renderText(item.nombre)")
              td(colspan='2' v-html="renderText(item.cargo)")
              td(colspan='3' v-html="renderText(item.centro)")

  Footer

</template>
<script>
export default {
  name: 'Inicio',
  data: () => ({
    configTitulos: {
      liderEquipo: 'ECOSISTEMA DE RECURSOS EDUCATIVOS DIGITALES',
      contenidoInstruccional: 'CONTENIDO INSTRUCCIONAL',
      desarrolloProducto:
        'DISEÑO Y DESARROLLO DE RECURSOS EDUCATIVOS DIGITALES',
      gestoresRepositorio: 'GESTORES DE REPOSITORIO',
    },
  }),
  computed: {
    creditosData() {
      return this.$config.creditos
    },
  },
  methods: {
    renderText(textObj) {
      let newText = ''
      if (Array.isArray(textObj)) {
        textObj.forEach((texto, index) => {
          newText += (index ? '<br/>' : '') + texto
        })
      } else {
        newText += textObj
      }
      return newText
    },
  },
}
</script>

<style lang="sass">
.creditos
  td, th
    border-color: $color-sistema-c
</style>
