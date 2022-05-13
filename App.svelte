<script>
    import Circulo from './componentes/Circulo.svelte';

    export let name;

    function GetRandom() {
        const nextNumber = Math.random() * 255;
        return Math.round(nextNumber);
    }
</script>


<h1>Welcome to {name}!</h1>
<img width="250" src="./icons/svelte.svg" alt="Svelte">

{#each Array(50) as x}
    <Circulo raio={ GetRandom()/2 + 25 } coordenadas={[GetRandom()*5 -30, GetRandom()*3 -30]} corRGB={[GetRandom(), GetRandom(), GetRandom()]}></Circulo>
{/each}
