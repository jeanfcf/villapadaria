<template>
    <div id="onde">
        <div class="onde-mapa">
            <iframe id="mapa-frame" src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d554.9162844411004!2d-40.50677842332488!3d-7.575665544701536!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x79fa9fa3e11ab23%3A0xa17eb45ad9a4bf07!2sVILLA%20GOURMET!5e0!3m2!1sen!2sbr!4v1589225770954!5m2!1sen!2sbr" width="600" height="450" frameborder="0" style="border-radius: 50px;" allowfullscreen="" aria-hidden="false" tabindex="0"></iframe>
        </div>
        <div class="onde-texto">
            <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Veniam, ipsam. Quam accusantium, optio minus adipisci fugiat, explicabo nulla, exercitationem expedita quas in ipsum doloribus aliquam itaque? Quaerat consequuntur dolores at?</p>
            <div class="onde-foto"/>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            
        }
    },
}
</script>

<style scoped>
    #onde{
        display: flex;
        justify-content: space-around;
        align-items: center;
        width: 100%;
        min-height: 10vh;
        padding-top: 5%;
        padding-bottom: 5%;
        background-color: #DCDFDE;
    }

    .onde-texto{
        text-align: center;
        display: flex;
        flex-direction: column;
        justify-content: space-around;
        align-items: center;
        width: 45%;
    }
    .onde-texto p{
        margin-bottom: 4%;
    }
    .onde-foto{
        width: 80%;
        height: 250px;
        background-color: #c4c4c4;
    }

    @media screen and (max-width: 1160px){
        #mapa-frame{
            width: 440px;
            height: 330px;
        }
    }
    @media screen and (max-width: 975px){
        #onde{
            flex-direction: column-reverse;
            justify-content: center;
        }
        #mapa-frame{
            width: 700px;
            height: 400px;
        }
        .onde-texto{
            width: 70%;
            margin-bottom: 5%;
        }
        .onde-texto p{
            font-size: 20px;
        }
        .onde-foto{
            width: 100%;
            height: 30vh;
        }
    }
    @media screen and (max-width: 770px){

        #mapa-frame{
            width: 500px;
            height: 400px;
        }
    }

    @media screen and (max-width: 550px){

        .onde-texto p{
            font-size: 16px;
        }
        #mapa-frame{
            width: 300px;
            height: 300px;
        }

    }
</style>