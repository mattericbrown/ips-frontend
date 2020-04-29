<template>
  <div class="content">
    <div class="header">
      <h1 class="header__text">10 Best Photo Apps For Incredible iPhone Photography (2020 Edition)</h1>
      <div class="header__divide"></div>
    </div>
    <div class="blog">
      <p class="blog__text">How do you capture more interesting travel photos with your iPhone? How do you avoid taking the same cliché vacation photos that everyone else takes? I recently interviewed Steffen Geldner – a talented iPhone photographer with a passion for travel. In this article, Steffen reveals 7 tips for shooting beautiful travel photos that will preserve the amazing memories of your trip. Read on to discover how to take better travel photos with your iPhone!</p>
      <div class="blog__image">
        <img srcset="../assets/img.jpg 300w, ../assets/img@2x.jpg 1000w" sizes="(max-width: 900px) 20vw, (max-width: 600px) 30vw, 300px" alt="photo 1" class="blog__image--main" src="../assets/img@3x.jpg">
      </div>
      <h2 class="blog__header">1. Research Your Destination To Find The Best Photo Opportunities</h2>
      <p class="blog__text">Before your trip, I recommend researching the destination to find the most interesting photo opportunities.</p>
      <p class="blog__text">I always research the location I’m traveling to. I do this extensively and obsessively!</p>
      <p class="blog__text">It’s up to you how much research you do. But you should definitely spend a bit of time looking up some great places to take pictures.</p>
      <p class="blog__text">So, what kind of research can you do?</p>
      <p class="blog__text">First, you could search for photos that other people have taken at the locations you’re planning to visit.</p>
      <p class="blog__text">Search on Instagram or Google to get an idea of the kinds of photos people take there.</p>
      <h2 class="blog__header">2. Capture Your Journey To Tell The Complete Story Of Your Travels</h2>
      <p class="blog__text">Travel photography isn’t just about photographing the destination.</p>
      <p class="blog__text">For a more complete photographic story, capture your journey to and from the location you’re visiting.</p>
      <p class="blog__text">If you’re traveling by plane, try to get a window seat where you have a view of the wing or propeller.</p>
      <p class="blog__text">And of course, you could capture a beautiful aerial view of clouds, mountains, or city lights as you’re flying above.</p>
      <p class="blog__text">Your journey will often involve several different types of transport. And they all offer great photo opportunities.</p>
      <p class="blog__text">Whether you’re traveling by car, taxi, bus, train, boat, or plane, try to capture some interesting photos.</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Content',
  // props: {
  //   msg: String
  // }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

  .content {
    position: relative;
    margin-top: 76px;
    max-width: 568px;
    left: 20vw;
  } 

  .header {

    &__text {
      font-weight: bold;
      font-size: 26px;
      line-height: 31px;
    }

    &__divide {
      width: 100%;
      height: 1px;
      border-bottom: 1px solid;
      border-image-source: linear-gradient(90deg, #AC519C 0.83%, #E5424F 100%);
      border-image-slice: 1;
    }
  }

  .blog {

    &__text {
      font-weight: 300;
      font-size: 16px;
      line-height: 24px;
    }

    &__image {
      &--main {
        margin: 20px 0;
        width: 100%;
      }
    }

    &__header {
      margin: 20px 0;
      font-weight: bold;
      font-style: normal;
      font-size: 18px;
      line-height: 22px;
      letter-spacing: -.9px;
    }
  }

  @media only screen and (max-width : 1386px) {
      .content {
        left: 16vw;
      }
  }

  @media only screen and (max-width : 1280px) {
      .content {
        left: 12vw;
      }
  }

  @media only screen and (max-width : 1200px) {
      .content {
        left: 10vw;
      }
  }

   @media only screen and (max-width : 1024px) {
      .content {
        left: 6vw;
      }
  }

  @media only screen and (max-width : 768px) {
      .content {
        left: 2vw;
      }
  }

   @media only screen and (max-width : 400px) {
      .content {
        position: relative;
        left: 0;
        width: 90%;
        max-width: 100vw;
        margin: 0 16px;

        &__button {
          position: absolute;
          margin: 0;
          left: 50%;
          transform: translateX(-50%);
        }
      }

      .blog {

        &__image {
          &--main {
            margin: 0;
            position: relative;
            width: 100vw;
            left: -24px;
          }
        }
      }
  }

</style>
