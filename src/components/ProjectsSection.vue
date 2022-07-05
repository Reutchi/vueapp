<template>
    <div class="project-section">

    <div class="bg"></div>
    <div class="section">
    <span>01</span>
    <h2>Sinder</h2>
    <p>A dating app — for single socks.</p>
    <a href="">Click me</a>
    </div>
   
    </div>
</template>

<script>
    export default {
        
    }
</script>

<style lang="scss" scoped >
.project-section{
    background-image: url(../assets/portofolio.png);
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
    width: 100%;
    padding: 250px;
    -webkit-mask-image: radial-gradient(circle, black 50%, rgba(0, 0, 0, 0.5) 50%);

        span{
            color: #808080;
            font-size: 69px;
            font-family: 'Palatino';
        }
        h2{
            font-size: 44px;
            color: #FFFFFF;
            font-weight: 400;
        }
        p{
            color: #7A7A7A;
            font-size: 17px;
            line-height: 32px;
        }
        
        
        
        
 }

</style>

