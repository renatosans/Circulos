
<script>
    export let raio;
    export let coordenadas;
    export let corRGB;

    function GetDiametro() {
        return raio * 2 + "px";
    }

    function GetCoordenadas(){
        return ";left:" + coordenadas[0] + "px" + ";top:" + coordenadas[1] + "px";
    }

    function GetCor(){
        return "border-color: rgb(" + corRGB[0] + ", " + corRGB[1] + ", " + corRGB[2] + ")";
    }

    function GetDimensoes() {
        return ";width:" + GetDiametro() + ";height:" + GetDiametro();
    }
</script>

<style>
    .circle{
        position: fixed;
        border-style: solid;
        border-width: 10px;
        border-radius: 50%;
        background-color: gray;
        opacity: 50%;
    }
</style>

<div class="circle" style="{ GetCor() + GetCoordenadas() + GetDimensoes()}"></div>
