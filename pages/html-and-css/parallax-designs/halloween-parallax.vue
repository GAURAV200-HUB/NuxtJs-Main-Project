<template>
  <div class="halloween-parallax">
    <section>
      <img
        id="bg"
        src="../../../assets/images/halloween-parallax/bg.jpg"
        alt="bg"
      />
      <img
        id="bats"
        src="../../../assets/images/halloween-parallax/bats.png"
        alt="bats"
      />
      <img
        id="castle"
        src="../../../assets/images/halloween-parallax/castle.png"
        alt="castle"
      />
      <img
        id="img"
        src="../../../assets/images/halloween-parallax/img.png"
        alt="img"
      />
      <img
        id="wolf"
        src="../../../assets/images/halloween-parallax/wolf.png"
        alt="wolf"
      />
    </section>
    <div class="sec">
      <div class="content">
        <h1>{{ heading }}</h1>
        <p>{{ para }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HalloweenPaeallax',
  data() {
    return {
      heading: 'Happy Halloween',
      para: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Quae repudiandae aperiam, ipsa nemo vel vitae sequi eligendi qui explicabo animi voluptas corporis vero a sint amet sunt placeat sed ab dolores tempore veniam totam earum. Ullam perferendis animi odit praesentium accusamus magnam laborum doloribus fugit rem ab debitis aliquam dignissimos impedit odio maxime quia officia, dicta necessitatibus laboriosam fugiat similique illo quisquam. Optio, placeat laborum? Totam quaerat aut aliquid reprehenderit, esse aperiam quae velit eligendi veniam mollitia fugiat ab minus voluptates vitae. Eligendi error alias repudiandae eos dicta iste doloribus voluptas ducimus quae qui expedita illo architecto et quidem, ullam sequi odit sit deleniti similique voluptatum voluptatibus veritatis incidunt ipsum! Doloribus quas tempore cumque architecto odit autem! Id ducimus quasi et hic eaque provident quae quibusdam nostrum nisi nam, sed, in quos dolorum recusandae similique itaque voluptatem necessitatibus magni velit molestias ullam? Molestias natus iste voluptatibus illo similique. Dolor, mollitia illo similique blanditiis accusamus, vero debitis numquam eos atque soluta, nesciunt eaque reiciendis quam placeat repellendus optio? Modi porro unde perspiciatis perferendis sed enim. Voluptatem explicabo magni iste autem sit voluptate provident, quibusdam commodi rem, reiciendis dicta, eligendi reprehenderit sunt impedit praesentium necessitatibus veniam. Cumque, a mollitia! Tempore laborum reiciendis neque sunt delectus praesentium perspiciatis molestias quia exercitationem beatae officia, ipsam facere unde explicabo. Quia maxime cupiditate, neque porro quidem repellat eius iusto magni accusantium placeat quibusdam, sed molestiae reiciendis eos? Praesentium ratione iusto quae reiciendis quod nihil quisquam veritatis sunt earum laudantium illum vero, repudiandae, ullam impedit dolorem similique eligendi aut incidunt, obcaecati laborum velit. Suscipit debitis quasi impedit aliquam magnam a laborum, explicabo harum, at, expedita animi enim. Iure ex tenetur assumenda ea quia eos rerum incidunt id aliquid nulla alias veniam, quisquam animi sit culpa reprehenderit laborum eius neque. Veniam eos commodi, in aliquid vitae sapiente. Optio!',
    }
  },
  mounted() {
    this.animation()
  },
  methods: {
    animation() {
      const gsap = this.$gsap
      gsap.to('#img', {
        x: 1500,
        y: 500,
        scrollTrigger: {
          scrub: 0.5,
        },
      })
      gsap.to('#wolf', {
        x: 400,
        scrollTrigger: {
          scrub: 0.5,
        },
      })
      gsap.to('#castle', {
        x: -100,
        scrollTrigger: {
          scrub: 0.5,
        },
      })
      gsap.to('#bats', {
        scale: 1.5,
        scrollTrigger: {
          scrub: 0.5,
        },
      })
    },
  },
}
</script>

<style lang="css" scoped>
.halloween-parallax section {
  position: relative;
  width: 100%;
  height: 100vh;
  overflow: hidden;
}

section img {
  position: absolute;
  top: 0;
  left: 0;
  max-width: 100%;
}

section::before {
  content: '';
  position: absolute;
  bottom: 0;
  width: 100%;
  height: 100px;
  background: linear-gradient(to top, #010405, transparent);
  z-index: 1;
}
</style>
