<script>

export default {
    name: 'JokesView',
    data() {
        return {
            joke: ''
        }
    },
    methods: {
        nextJoke() {
            const jokes = [
                'Seu cachorro nabunda cai no mar, vc deixa nabunda ou leva nabunda?',
                'Voce pinta como eu pinto?',
                'Tifu, tifu, tifu, quantos tifu deu?',
                'Jacaré em terrenos alagados anda,mais no secu anda?',
                'Tenho 1 Kg de arroz, seu cuzinho, ele é meu?',
                'Já viu o palhaço que se esconde de viado?',
                'Vou fazer um churrasco, 30 kg de carne, sera q da pra 20 comer?',
                'E a onça? aquela pintada que eu te dei',
                'Texto bom é o pequeno ou você gosta do grandão?',
                'Vamos apostar? Mil meu com mil seu',
                'Se eu passar roupa, você leva o ferro?',
                'Qual é o aumentativo de dacueba?',

            ];
            this.joke = jokes[Math.floor(Math.random() * jokes.length)];
        }
    },
    mounted() {
        this.nextJoke();
    }
}
</script>

<template>
    <div>
        <div>
            <h1>Bora rir um pouco...</h1>
            <p class="mt-4 mb-5 joke">
                {{ joke }}
            </p>
        </div>
        <div>
            <button class="btn btn-success btn-full mb-2" v-on:click="nextJoke">Próxima</button>
            <RouterLink to="/" class="btn btn-success btn-full">Voltar</RouterLink>
        </div>
    </div>
</template>