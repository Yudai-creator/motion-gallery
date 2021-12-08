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
            <a href="#email">Get Notify</a>
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
          
          <a href="#anim" class="hero_btn">Learn More</a>
          
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
        <div class="custom-shape-divider-top-1638991973">
          <svg data-name="Layer 1" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 120" preserveAspectRatio="none">
            <path d="M1200 0L0 0 598.97 114.72 1200 0z" class="shape-fill"></path>
          </svg>
        </div>
      </section>

      <section id="anim" class="main_slide-show">
        <h2>Making use of utility classes to call the animations</h2>
        <div class="slider">
          
          <div class="el-wrapper">
            <div class="el el-3"></div>
            <!--<p>Meka keme</p>-->
          </div>
          
          <div id="like-wrapper">
            <div class="el el-1"></div>
            <p>.swipe-up</p>
          </div>
          
          <div class="el-wrapper">
            <div class="el el-2"></div>
            <!--<p>El buYa</p>-->
          </div>
          
          <svg id="cursor" xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24">
            <path d="M20.978 13.21a1 1 0 0 0-.396-1.024l-14-10a.999.999 0 0 0-1.575.931l2 17a1 1 0 0 0 1.767.516l3.612-4.416 3.377 5.46 1.701-1.052-3.357-5.428 6.089-1.218a.995.995 0 0 0 .782-.769z" fill="#EEEEEE"/>
          </svg>
        </div>
      </section>

      <section class="main_message">

      </section>

      <footer id="email">
        <div class="footer_text">
          <h2>Get notify</h2>
          <p>When the project comes out I'll let you know</p>
        </div>
        <form action="" class="main_form">
          <input class="form_input" type="text" placeholder="Leave your email">
          <input class="form_btn" type="submit" value="Send">
        </form>
        <hr>
        <div class="footer_brand">
          <p>Proudly build by </p>
          <img src="~/static/01.2.svg"/>
        </div>
      </footer>
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

//Main content
main{
  position: relative;

  
  //Hero section
  .hero{
    position: relative;
    margin-top: 1rem;
    padding: 2rem;
    .hero_text-wrapper{
      position: relative;
    }

    //Circles for decoration
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


      //Call to action
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

  //Info about the project
  .main_info{
    background-color: $secondary;
    padding: 2rem;
    position: relative;

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

    .custom-shape-divider-top-1638991973 {
      position: absolute;
      bottom: -60px;
      left: 0;
      width: 100%;
      overflow: hidden;
      line-height: 0;
    }

    .custom-shape-divider-top-1638991973 svg {
      position: relative;
      display: block;
      width: calc(100% + 1.3px);
      height: 60px;
    }

    .custom-shape-divider-top-1638991973 .shape-fill {
      fill: #393E46;
    }
  }


  //Animations
  .main_slide-show{
    padding: 2rem;
    text-align: center;
    position: relative;
    top: 50px;

    .slider{
      position: relative;
      padding: 2rem;
      margin-top: 2.5rem;

      display: flex;
      justify-content: space-between;

      div[id]{
        color: $accent_tone1;
        font-weight: 600;
      }

      .el-wrapper{
        position: relative;
        bottom: 45px;

        opacity: .2;

        .el-2{
          width: 40px;
          height: 40px;
          background-color: $accent_tone1;
          border-radius: 10px;
        }

        .el-3{
          width: 40px;
          height: 40px;
          background-color: $accent_tone1;
          border-radius: 10px;
        }
      }

      #like-wrapper{
        position: relative;

        .el-1{
          width: 45px;
          height: 45px;
          background-color: $accent;
          border-radius: 50%;
        }
      }

      #cursor{
        opacity: .3;
        animation: cursor--move 3s infinite alternate cubic-bezier(0.65, 0.05, 0.36, 1);
      }

      @keyframes swipe--up {
        to{
          width: 40px;
          height: 40px;
          //fill: #70f8cb;

          transform: translateY(-5px);
        }
      }

      @keyframes cursor--move {
        from{
          transform: translate(0,0);
        }
        to{
          transform: translate(-98px, 18px);
          opacity: 1;
        }
      }



      // #like::after{
      //   content: 'perro';
      //   position: absolute;
      //   top: 20%;
      //   color: white;
      // }

      // #message{
      //   position: relative;
      //   bottom: 50px;
      //   right: 50px;
      // }

      // #check-square{
      //   position: relative;
      //   bottom: 50px;
      //   left: 50px;
      // }
    }
  }

  .main_message{
    background-color: $secondary;
    padding: 3rem;
  }
}

footer{
  background-color: $primary;
  padding: 2rem;

  .main_form{
    text-align: center;

    .form_input{
      border-radius: 5px 0 0 5px;
      padding: .25rem;

      border: none;
    }

    .form_btn{
      position: relative;
      right: 5px;

      border-radius: 0 5px 5px 0;
      padding: .25rem;
      background-color: $accent_tint1;
      font-weight: 600;
      color: $primary;

      border: none;
    }
  }

  .footer_text{
    text-align: center;
    margin-bottom: 1rem;
  }

  hr{
    border-color: $accent;
    margin-top: 2rem;
    margin-bottom: 1.5rem;
  }

  .footer_brand{
    position: relative;
    display: flex;
    justify-content: center;

    img{
      position: absolute;
      top: 60%;
    }
  }
}



</style>
