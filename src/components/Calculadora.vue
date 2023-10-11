    <template>
        <div>
        <input v-model="numero1" @input="calcularResultado" />
        <select v-model="operacao" @change="calcularResultado">
            <option value="soma">+</option>
            <option value="subtracao">-</option>
            <option value="multiplicacao">*</option>
            <option value="divisao">/</option>
        </select>
        <input v-model="numero2" @input="calcularResultado" />
        <p>Resultado: {{ resultado }}</p>
        </div>
    </template>
    
    <script>
    export default {
        data() {
        return {
            numero1: 0,
            numero2: 0,
            operacao: "soma",
            resultado: 0,
        };
        },
        methods: {
        calcularResultado() {
            const num1 = parseFloat(this.numero1);
            const num2 = parseFloat(this.numero2);
    
            if (!isNaN(num1) && !isNaN(num2)) {
            switch (this.operacao) {
                case "soma":
                this.resultado = num1 + num2;
                break;
                case "subtracao":
                this.resultado = num1 - num2;
                break;
                case "multiplicacao":
                this.resultado = num1 * num2;
                break;
                case "divisao":
                this.resultado = num1 / num2;
                break;
            }
            } else {
            this.resultado = "Erro";
            }
        },
        },
    };
    </script>