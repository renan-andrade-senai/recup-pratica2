<template>
  <div class="row justify-content-center">
    <div class="col-md-8">
      <h2 class="mb-4">Cadastrar Novo Jogo</h2>

      <!-- TODO 14 — Crie um formulário com os seguintes campos:
             - Título           (input text)
             - Plataforma       (input text ou select com opções)
             - Gênero           (input text)
             - Ano de Lançamento (input number)
             - Disponível       (select com opções: Disponível / Locado)

           Use v-model para vincular cada campo à variável "novoJogo".
           Ao enviar o formulário, chame a função "cadastrarJogo".

           Adicione também:
             - Um botão "Salvar"
             - Um botão "Cancelar" que volta para /jogos -->
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'
import { useRouter } from 'vue-router'
import axios from 'axios'
// TODO 15 — Importe a interface Jogo do arquivo de tipos

const router = useRouter()
const API_URL = 'http://localhost:3000/jogos'

// TODO 16 — Crie a variável reativa "novoJogo" com os campos
//   do jogo, sem o "id" (que é gerado automaticamente pela API).
//   Dica: use Omit<Jogo, 'id'> para tipar o objeto sem o campo id.

// TODO 17 — Crie a função "cadastrarJogo" que:
//   1. Faz uma requisição POST para a API_URL com os dados de "novoJogo"
//   2. Redireciona para /jogos após o cadastro
</script>