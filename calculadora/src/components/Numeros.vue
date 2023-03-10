<template>
    <main>
        <div class="numeros">
            <table>
                <tr>
                    <th><button>C</button></th>
                    <th><button>÷</button></th>
                    <th><button>-</button></th>
                    <th><button>x</button></th>
                </tr>
                <tr>
                    <th><button>1</button></th>
                    <th><button>2</button></th>
                    <th><button>3</button></th>
                    <th><button>+</button></th>
                </tr>
                <tr>
                    <th><button>4</button></th>
                    <th><button>5</button></th>
                    <th><button>6</button></th>
                    <th><button>=</button></th>
                </tr>
                <tr>
                    <th><button>7</button></th>
                    <th><button>8</button></th>
                    <th><button>9</button></th>
                    <th><button>0</button></th>
                </tr>
        </table>
        </div>
    </main>
</template>
<script>
export default{
    name: "Numeros"
}
</script>

<style>
.numeros{
grid-column: span 4;
display: flex;
justify-content: center;
align-items: center;
padding: 20px;
font-size: 2.1em;
overflow: hidden;
}
.numeros button{
    background-color: rgb(6, 10, 27);
    color: beige;
    padding: 20px;

}
th .sinal{
    background-color: rgb(6, 10, 27);
    color: beige;
    width: 50px;
    height: 100px;

    

}

</style>