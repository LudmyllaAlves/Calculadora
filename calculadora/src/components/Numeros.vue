
<template>
    <main>
        
        <div class="numeros">
            <table>
                <tr>
                    <th><button @click="limparMenu()">c</button></th>
                    <th><button @click="dividir()">÷</button></th>
                    <th><button @click="subtrair()">-</button></th>
                    <th><button @click="multiplicar()">x</button></th>
                </tr>
                <tr>
                    <th id="numero"><button>1</button></th>
                    <th id="numero"><button>2</button></th>
                    <th id="numero"><button>3</button></th>
                    <th><button @click="somar()">+</button></th>
                </tr>
                <tr>
                    <th id="numero"><button>4</button></th>
                    <th id="numero"><button>5</button></th>
                    <th id="numero"><button>6</button></th>
                    <th><button @click="resposta()">=</button></th>
                </tr>
                <tr>
                    <th id="numero"><button>7</button></th>
                    <th id="numero"><button>8</button></th>
                    <th id="numero"><button>9</button></th>
                    <th id="numero"><button>0</button></th>
                </tr>
        </table>
        </div>
    </main>
</template>
<script>
export default{
    name: "Numeros",
    data(){
        return{
            valorCorrente: '',
            numeroAnterior: null,
            operador: null,
            operadorClicado: false,
        }
    },
    methods:{
        
        limparMenu(){
            this.valorCorrente = '';
        },
        somar(){
            this.operador = (num1, num2) => num1 + num2;
            this.setarValor();
        },
        subtrair(){
            this.operador = (num1, num2) => num1 - num2;
            this.setarValor();
        },
        dividir(){
            this.operador = (num1, num2) => num1 / num2;
            this.setarValor();
        },
        multiplicar(){
            this.operador = (num1, num2) => num1 * num2;
            this.setarValor();
        },
        resposta() {
        this.valorCorrente = `${this.operador(
        parseFloat(this.numeroAnterior),
        parseFloat(this.valorCorrente),
        )}`;
        this.numeroAnterior = null;
    },
    }
}
</script>

<style>
body{
    background-color: rgba(162, 163, 163, 0.74);
}
.numeros{
grid-column: 4;
display: flex;
justify-content: center;
align-items: center;
padding: 20px;
font-size: 2.1em;
overflow: hidden;
}
.numeros button{
    background-color: rgb(6, 10, 27);
    color: #787b9b;
    padding: 20px;
}
th .sinal{
    background-color: rgb(6, 10, 27);
    color: #787b9b;
    width: 50px;
    height: 100px;

}

</style>