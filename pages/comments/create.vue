<template>
    <div>
        <div class="container">
            <form @submit.prevent="submitForm">
                <h1>Novo comentário</h1>
                <div class="field" >
                    <label for="name">Nome: </label>
                    <input v-model="form.name" name="name" placeholder="Escreva aqui..." type="text" required>
                </div>
                <div class="field" >
                    <label for="email">Email:</label>
                    <input type="email" v-model="form.email" name="name" placeholder="Escreva aqui..." required>
                </div>
                <div class="field" >
                    <label for="body">
                        <i class="far fa-edit"></i>Conteúdo:
                    </label>
                    <textarea v-model="form.body" name="body" placeholder="Escreva aqui..." required></textarea>
                </div>
                <button class="btn" type="submit">Enviar</button>
            </form>
        </div>

    </div>
</template>

<script>
export default {
    layout: 'customLayout',
    data() {
        return {
            form: {
                title: "",
                body: "",
                email: "", 
                id: 1
            }
        }
    },
    methods: {
        submitForm() {
            this.$axios
                .post('/comments', this.form)
                .then( res => {
                    alert("Funcionou!");
                
                })
                .catch( err => {
                    alert("Deu erro!");
                })     
        },
        cleanAll() {
            this.form.title = "";
            this.form.body = "";
            this.form.email = "";
        }
    }
}
</script>


<style scoped>
h1 {
font-family: 'Montserrat', Arial, sans-serif;
display: block;
font-weight: 400;
text-align: center;
}
.container {

color: black;
display: flex;
justify-content: center;
align-items: center;
min-height: 82vh;
}



form {
display: flex;
flex-direction: column;
padding: 50px 40px;
background: #eceffc;
border-radius: 10px;
box-shadow: 2px 2px 2px 2px rgba(128, 128, 128, 0.7);
width: 550px;
height: 600px;
margin-bottom: 20px;
}


form h1, .field {
margin: 0 0 24px 0;
}

.btn {
color: #ECF0F1;
background-color: #50D18D;
padding: 10px;
border-radius: 1.25rem;
cursor: pointer;
border: none;

font-weight: 400;
font-size: 50px;
}

input, textarea, .btn {
margin: 0;
font-family: inherit;
font-size: inherit;
line-height: inherit;
width: 100%;
}
textarea {
min-height: 180px;    
}
input, textarea {
padding: 10px 20px 10px 20px;
}
label {
font-size: 19px;
}
</style>