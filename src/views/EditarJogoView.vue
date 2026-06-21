<template>
  <div class="row justify-content-center">
    <div class="col-md-8">
      <h2 class="mb-4">Editar Jogo</h2>

      <!-- TODO 18 — Exiba o formulário de edição com os mesmos campos
           do formulário de cadastro.
           Os campos já devem estar preenchidos com os dados do jogo
           carregados da API.

           Use v-model para manter os campos vinculados à variável "jogo".
           Ao enviar, chame a função "atualizarJogo".

           Adicione também:
             - Um botão "Salvar alterações"
             - Um botão "Cancelar" que volta para /jogos -->
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref, onMounted } from 'vue'
import { useRouter, useRoute } from 'vue-router'
import axios from 'axios'
// TODO 19 — Importe a interface Jogo do arquivo de tipos

const router = useRouter()
const route = useRoute()
const API_URL = 'http://localhost:3000/jogos'

// TODO 20 — Obtenha o ID do jogo a partir dos parâmetros da rota.
//   Dica: use route.params.id
//   Atenção: route.params retorna string — converta para número
//   usando Number() antes de usar nas requisições.

// TODO 21 — Crie a variável reativa "jogo" do tipo Jogo,
//   com valores iniciais vazios/padrão para cada campo.

// TODO 22 — Crie a função "buscarJogo" que:
//   1. Faz uma requisição GET para API_URL/id
//   2. Armazena o resultado na variável "jogo"
//   (isso vai preencher automaticamente os campos do formulário via v-model)

// TODO 23 — Crie a função "atualizarJogo" que:
//   1. Faz uma requisição PUT para API_URL/id com os dados de "jogo"
//   2. Redireciona para /jogos após salvar

// TODO 24 — Use onMounted para chamar "buscarJogo" quando
//   a página for carregada
</script>