<template>
        <section class="hero"> 
            <div class="typing-section">
                <h1 class="typed-text">{{typeValue}}
                <span class="cursor" :class="{'typing':typeStatus}">&nbsp;</span>
                </h1>
            </div>
            <div class="hero-desc">
                <p>With my knowledge as a web developer, design experience, and a great sense of detail, I will create amazing responsive websites. 🚀</p>
            </div>
            <span class="arrow"><img src="../assets/arrow.svg" alt=""></span>
        </section>
</template>

<script>

export default {
 
  data:() => {
    return {
        typeValue: "",
        typeStatus: false,
        typeArray: ['Hello, You.'],
        typingSpeed: 200,
        erasingSpee: 100,
        newTextDelay: 2000,
        typeArrayIndex: 0,
        charIndex: 0,
    }
      
    },
     methods: {
        typeText(){
              if(this.charIndex < this.typeArray[this.typeArrayIndex].length){
                if(!this.typeStatus)
                this.typeStatus = true;

                this.typeValue += this.typeArray[this.typeArrayIndex].charAt(this.charIndex)
                this.charIndex += 1;

                setTimeout(this.typeText, this.typingSpeed)
              }
              else{
                this.typeStatus = false;
              }
        },
        eraseText(){

        }
     },
     created(){
        setTimeout(this.typeText, this.newTextDelay + 200)
     }
  }
  
</script>

<style lang="scss">
.hero{

    h1{
        .cursor{
            display: inline-block;
            margin-left: 3px;
            width: 4px;
            background-color: lightgray;
            animation: cursorBlink 1s infinite;
        }
        .span.cursor.typing{
            animation: none;
        }
        max-width: 500px;
        padding: 120px 0 0 25px;
        font-size: 90px;
        color: #333333;
        line-height: 150px;

    }
    .arrow{
        display: flex;
        justify-content: center;
        cursor: pointer;
        margin-bottom: 20px;
    }

}


@keyframes cursorBlink{
    49% { background-color: lightgray;}
    50% { background-color: transparent;}
    99% { background-color: transparent;}

}


.hero-desc{
    padding: 100px 0 50px;

   p {  
    padding: 10px;
    font-size: 25px;
    font-weight: regular;
    max-width: 70%;
    margin: 0 auto;
   }
   
   p + p{
    margin-top: 10px;
   }
   
}


</style>
