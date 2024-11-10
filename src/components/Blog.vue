<template>
  <div class="container">
    <section class="blog">
      <div class="blog__content">
        <div
          class="blog__content__cont"
          v-for="article in filteredArticles"
          :key="article.id"
        >
          <h1>{{ article.title }}</h1>
          <img :src="require(`@/assets/img/${article.img}`)" :alt="article.tag" class="blog__img"/>
          <p>{{ article.text }}</p>
        </div>
      </div>

      <div class="blog__tags">
        <h1>Tags</h1>
        <div class="blog__tags__btns">
          <button class="blog-btn" @click="sort('Kitchen')">Kitchen</button>
          <button class="blog-btn" @click="sort('Bedroom')">Bedroom</button>
          <button class="blog-btn" @click="sort('Building')">Building</button>
          <button class="blog-btn" @click="sort('Architecture')">
            Architecture
          </button>
          <button class="blog-btn" @click="sort('Kitchen-planning')">
            Kitchen planning
          </button>
          <button class="blog-btn" @click="sort('Bathroom')">Bathroom</button>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  data() {
    return {
      filteredArticles: [
        {
          id: 1,
          tag: "Kitchen",
          title:
            "CUTTING-EDGE COUNTERTOP IDEAS FOR YOUR MODERN AMERICAN KITCHEN",
          img: "blog-kitchen1.png",
          text: "A quintessential modern kitchen may be sleek, sophisticated and simple, but if you look closely, you’ll realize that it takes a lot of work to turn simplicity into brilliance.The modern American kitchen is the result of innovation and creativity—a product of meticulous craftsmanship that defines function and style. Thanks to an array of modern materials, we now have the power to make big changes with small accessories, focusing on more than just aesthetic beauty.",
          date: "26 December,2022 ",
        },
      ],
      articles: [
        {
          id: 1,
          tag: "Kitchen",
          title:
            "CUTTING-EDGE COUNTERTOP IDEAS FOR YOUR MODERN AMERICAN KITCHEN",
          img: "blog-kitchen1.png",
          text: "A quintessential modern kitchen may be sleek, sophisticated and simple, but if you look closely, you’ll realize that it takes a lot of work to turn simplicity into brilliance.The modern American kitchen is the result of innovation and creativity—a product of meticulous craftsmanship that defines function and style. Thanks to an array of modern materials, we now have the power to make big changes with small accessories, focusing on more than just aesthetic beauty.",
          date: "26 December,2022 ",
        },
        {
          id: 2,
          tag: "Kitchen",
          title: "YOUR QUICK GUIDE TO MODERN CABINETRY",
          img: "blog-kitchen2.png",
          text: "It’s amazing what small tweaks in interior design can do to your kitchen. From high-end finishes to wood textures, there’s a world of options just waiting to be discovered!         In recent years, we’ve seen modern kitchen styles dominating American homes, and prompting homeowners to invest in innovative ideas.   Choosing the right cabinetry forms the crux of kitchen innovation as it adds a strikingly unique touch that punctuates your kitchen, while giving you an opportunity to be creative!",
          date: "01 May,2023",
        },
        {
          id: 3,
          tag: "Bedroom",
          title: "Bedroom Lighting Tips to Make Your Bedroom Feel Extra Cosy",
          img: "blog-bedroom1.jpg",
          text: "The perfect lighting for the bedroom is essential to ensure warmth and comfort in the room. In addition, different light sources can enhance the decor and bring much more practicality to everyday life. There is a wide variety of lighting options; that can help you create the perfect ambience in your room. There are countless ways to use light to your advantage and brighten up your room smartly and stylishly—whether direct lighting through ceiling light fixtures, indirect lighting, or lampshades on top of the nightstand or bedside wall lights.",
          date: "20 July,2023",
        },
        {
          id: 4,
          tag: "Bedroom",
          title: "Essential bedroom lighting tips",
          img: "blog-bathroom2.jpg",
          text: "Articulated wall light: This type of sconce is ideal, if you desire a focus on books or even turn to the ceiling and create an indirect lighting point.Deflector Lamps: For bedside pendants, deflector lamps are an excellent option because they have a mirrored layer on the underside that avoids disturbing the eyes when lying down.  Tube light bulb: For curtain or ceiling mouldings lighting, tubular bulbs are recommended instead of LED strips, as they cast light almost all around them, making the lighting softer and producing fewer shadows. ",
          date: "12 January,2023",
        },
        {
          id: 5,
          tag: "Bathroom",
          title: "Modern Bathroom Vanity Ideas",
          img: "blog-bathroom1.jpg",
          text: "The bathroom vanity is one of the first places most people head to before beginning the day—so, it's a good idea to give some serious thought to how you want it to look and feel.",
          date: "18 March,2023",
        },
        {
          id: 6,
          tag: "Bathroom",
          title: "Modern Bathroom Ideas That Go Off the Beaten Path",
          img: "blog-bathroom2.jpg",
          text: "If your bathroom design is feeling lackluster, look no further for innovative design inspiration. From a converted enclosed deck to a shower that's steps away from a private garden, these unique spaces are sure to ignite your creativity",
          date: "09 April,2023",
        },
        {
          id: 7,
          tag: "Kitchen-planning",
          title: "Kitchen Floor Plans 101: Layouts, Tools, Designs, and Expert Tips",
          img: "kitchen-plan1.jpg",
          text: "A kitchen floor plan shows the arrangement of cabinets, counters, sink and major appliances in a given space. That’s the simple definition, but as anyone who has undertaken kitchen design or redesign knows, managing the multiple elements of a modern kitchen is challenging.",
          date: "23 May,2024",
        },
        {
          id: 8,
          tag: "Architecture",
          title: "The Importance of Architectural Design for Houses",
          img: "arcitecture1.png",
          text: "Architecture has always been one of the most fascinating things for humans for a long time. People are still amazed by seeing structures like the great pyramids, the leaning tower of Pisa, the Taj Mahal, etc. Since the world has evolved much if you compare the old times. Due to that the demands and requirements of people have also changed very much. With the advanced and efficient construction methods, you don’t need much effort to make your home or office great with exactly the features that you want. This article is going to be all about architectural designs for houses. As more and more people are searching for ways to build homes of their dreams, this article is going to help them all. Let us start this article without much delay. Since this article is going to start from fundamentals through other advanced concepts, you need to spend a few moments and it will be highly beneficial for you.",
          date: "15 February,2024",
        },
        {
          id: 8,
          tag: "Building",
          title: "‘Recession is underway’ for home builders",
          img: "building1.png",
          text: "The housing industry downturn is poised to push the U.S. economy into a mild recession this year, according to the National Association of Home Builders’ chief economist.",
          date: "1 February,2023",
        },
      ],
    };
  },
  methods: {
    sort(tag) {
      this.filteredArticles = this.articles.filter((el) => el.tag === tag);
    },
  },
};
</script>

<style lang="scss" scoped>
$mainTextColor: #292f36;
$colorTextGray: #4d5053;
$widthContainer: 1000px;

.blog-btn {
  color: $mainTextColor;
  text-align: center;
  font-family: Jost;
  font-size: 18px;
  font-style: normal;
  font-weight: 400;
  line-height: 125%;
  padding: 9px 30px;
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 10px;
  border-radius: 10px;
  background: #f4f0ec;
  border: none;
  cursor: pointer;
}
.blog-btn:hover {
  background-color: $mainTextColor;
  color: #fff;
}
.blog {
  display: grid;
  grid-template-columns: 70% auto;
  gap: 20px;
  &__content {
    display: flex;
    flex-wrap: wrap;

  }
  &__img{
    max-width: 100%;
    max-height: 100%;
    overflow: hidden;
  }
  &__tags {
    h1 {
      color: $mainTextColor;
      font-family: "DM Serif Display";
      font-size: 25px;
      font-style: normal;
      font-weight: 400;
      line-height: 125%;
    }
    &__btns {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
    }
  }
}
@media(max-width: 600px){
  .blog {
  display: flex;
  flex-direction: column-reverse;
  gap: 10px;
  }
}

</style>
