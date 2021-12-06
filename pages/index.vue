<template>
  <div class="container">
    <header>
      <div class="header_text-wrapper">
        <CircleElement style="left: 80%; top: -25%"/>
        <p>Motion<span>Gallery</span></p>
      </div>
      <nav>
        <ul>
          <li>
            <a href="#">Get Notify</a>
          </li>
        </ul>
      </nav>
    </header>
    <main>
      <div class="hero">
        <div class="hero_text-wrapper">
          <CircleElement style="left: -5%; top: -5%"/>
          <h1>Spice up your website with some nice motion</h1>
        </div>
        <div class="hero_arts">
          
          <div class="max-circle">
            <CircleElement/>
          </div>
          <div class="min-circle">
            <CircleElement/>
          </div>
          
          <a href="#" class="hero_btn">Learn More</a>
          
          <div class="hero_arts-circles">
            <CircleElement style="position: relative; margin: 1rem"/>
            <CircleElement style="position: relative; margin: 1rem"/>
            <CircleElement style="position: relative; margin: 1rem"/>
          </div>
        </div>
      </div>

      <section class="main_info">
        <h2>What to expect</h2>
        <p>
          Motion Gallery is an animation library with custom animations to help 
          developers improve their websites interaction with motion.
        </p>
        <br>
        <p>
          Using physical movement, micro-interactions and displacements made with cubic-bezier curves.
        </p>

        <div class="circles">
          <CircleElement style="position: relative; border: 5px solid #232931"/>
          <CircleElement style="position: relative; margin: 1rem"/>
          <CircleElement style="position: relative; margin: 1rem"/>
        </div>

        <h3>
          Simple animations to enrich you UI
        </h3>
      </section>

      <section class="main_slide-show">
        <h2>Making use of utility classes to call the animations</h2>
      </section>
    </main>
  </div>
</template>

<script>
import CircleElement from '../components/CircleElement.vue'

export default {
  components:{
    CircleElement
  }
}
</script>

<style lang="scss">
@import '~assets/scss/variables';

*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body{
  background-color: $primary;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  color: $text_color;
}


//Navigation
header{
  padding: 1.5em;
  display: flex;
  justify-content: space-between;

  nav{
      ul{
        li{
          display: inline;

          a{
            text-decoration: none;
            margin-left: 1rem;
            padding: .4rem;
            border: 2px solid $accent;
            border-radius: 20px;
            color: $accent_tint1;

            transition: all .3 ease-in-out;

            &:hover{
              color: $accent_tone1;
            }
          }
        }
      }
    }

  .header_text-wrapper{
    position: relative;
    p{
      color: $text_color;
      font-weight: 600;

      span{
        color: $accent;
      }
    }
  }
  
}

main{
  position: relative;

  
  .hero{
    position: relative;
    margin-top: 1rem;
    padding: 2rem;
    .hero_text-wrapper{
      position: relative;
    }

    .hero_arts{
      display: flex;
      flex-direction: column;
      align-items: center;
  
      position: relative;
      margin-top: 2rem;
      .max-circle{
        width: 200px;
        height: 200px;
        border-radius: 50%;
        background-color: $accent;
      }

      .min-circle{
        width: 100px;
        height: 100px;
        border-radius: 50%;
        background-color: $accent_tone1;

        margin-top: 2rem;
      }

      .hero_btn{
        margin-top: 2rem;
        padding: .5rem;
        border-radius: 20px;
        text-decoration: none;
        background-color: $accent_tint1;
        color: $primary;
        font-weight: bold;

        transition: all .3s ease-in-out;

        &:hover{
          background-color: $accent_tone1;
        }
      }

      .hero_arts-circles{
        padding: 2rem;
        position: relative;
        display: flex;
        justify-content: space-between;
      }
    }
  }

  .main_info{
    background-color: $secondary;
    padding: 2rem;

    h2{
      position: relative;

      &::before{
        content: '';
        position: absolute;
        top: -25%;
        width: 50px;
        height: 8px;
        background-color: $accent;
      }
    }

    p{
      margin-top: 1rem;
    }
  }


  .main_slide-show{
    padding: 2rem;
    text-align: center;
  }
}



</style>
