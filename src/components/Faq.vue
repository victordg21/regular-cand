<script>
export default {
    data() {
        return {
            faqs: [
                { question: 'Estou com minha candidatura deferida. Sou obrigado a ter advogado/a e contador/a?', answer: 'Sim. Pela Legislação, Resolução TSE 23.607, de 2019, í obrigatório constituir advogado/a, assim como contratar profissional habilitado em contabilidade.', showAnswer: false },
                { question: 'Quando terei o meu CNPJ de campanha?', answer: 'O CNPJ será emitido pela Receita Federal e disponibilizado em seu site em até 3 (três) uteis, após o recebimento pela Justiça Eleitoral o requerimento de registro da candidatura.', showAnswer: false },
                { question: 'O que devo saber para abrir a conta de campanha?', answer: 'a) que os bancos são obrigados a abrir a conta em até 3 (três) dias (Lei nº 9.504, de 1997); b) que é da sua escolha a instituição bancária; c) que não precisa de qualquer depósito inicial; d) que deve ser aberta conta para cada fonte de recursos doados.', showAnswer: false },
                { question: 'Quantas contas de campanha, devo ter?', answer: 'Cada conta de campanha é para uma fonte de doação. São elas: “Doação de Pessoas Físicas”; “Doação do Fundo Partidário”, “Doação do Fundo Especial de Financiamento de Campanha (FEFC)”.', showAnswer: false },
                { question: 'As três contas são obrigatórias?', answer: 'A Conta de “Doação Pessoa Física” é obrigatórias. As outras, que pode ser até mais 2 (duas) para candidatos homens e até mais 4 (quatro) para candidatas mulheres, só no caso de recebimento de recursos provenientes das respectivas fontes “Doação do Fundo Partidário” e “Doação do Fundo Especial de Financiamento de Campanha (FEFC)”.', showAnswer: false },
                { question: 'Por que no caso de candidatas mulheres há exigências por maior número de contas?', answer: 'Pelo fato dos recursos provenientes de “Doação do Fundo Partidário” e de “Doação do Fundo Especial de Financiamento de Campanha (FEFC)” se dividirem em duas contas especificas para cada uma das fontes. Sendo elas: “Doação do Fundo Partidário” e “Doação do Fundo Partidário Mulher; “Doação do Fundo Especial de Financiamento de Campanha (FEFC)” e “Doação do Fundo Especial de Financiamento de Campanha (FEFC) Mulher”.', showAnswer: false },
                { question: 'Quais os documentos necessários para abrir a minha conta de campanha?', answer: 'São os seguintes: a) Rac(Requerimento de Abertura de Conta Bancária), o qual será emitido através da página dos Tribunais Eleitorais na Internet; b) Comprovante do CNPJ para as eleições, disponível na página da Secretaria da Receita Federal do Brasil na Internet; Nomes dos/as responsáveis pela movimentação da conta bancária com endereço atualizado e respectivos documentos pessoais.', showAnswer: false },
                { question: 'Devo comprovar recebimento de recursos?', answer: 'Sim. O/A candidato/a deve em até 72 h (setenta e duas horas) apresentar à Justiça Eleitoral a doação, contados a partir da data de recebimento.', showAnswer: false },
                { question: 'Em que o RegularCand me ajuda?', answer: 'O RegularCand é uma aplicação web que lhe garante Advogados(as) e Contadores(as) e a interação entre as respectivas assessorias especializadas e obrigatórias em campanha e os responsáveis pela sua campanha, garantido, portanto, a segurança em favor da regularidade no processo de registro, campanha e prestação de contas. A ajuda é lhe deixar tranquilo para conseguir votos.', showAnswer: false },
            ]
        };
    },

    methods: {
        toggleAnswer(index) {
            this.faqs.forEach((faq, i) => {
                if (i === index) {
                    faq.showAnswer = !faq.showAnswer;
                } else {
                    faq.showAnswer = false;
                }
            });
        }
    },
};
</script>

<template>
    <section class="container px-5 lg:px-0 py-20"><!--FAQ-->
        <h2 class="text-4xl text-center pb-8">Perguntas Frequentes</h2>
        <div v-for="(faq, index) in faqs" :key="index">
            <div class="faq-item text-lg font-medium">
                <div :style="[faq.showAnswer ? 'border-top-left-radius: 6px; border-top-right-radius: 6px;' : 'border-radius: 6px;']" class="faq-question" @click="toggleAnswer(index)">
                    <h3 class="">{{ faq.question }}</h3>
                    <span v-if="faq.showAnswer">&#8722;</span><span v-else>&#43;</span>
                </div>
                <transition name="faq-slide">
                    <div v-if="faq.showAnswer" class="faq-answer">{{ faq.answer }}</div>
                </transition>
            </div>
        </div>
    </section>
</template>

<style scoped>

.container{
    max-width: 1280px;
    width: 100%;
    margin: 0 auto;
}

.faq-item {
    margin-bottom: 20px;
}

.faq-question {
    cursor: pointer;
    background-color: #DFCCA5;
    padding: 15px;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.faq-answer {
    border-bottom-left-radius: 6px;
    border-bottom-right-radius: 6px;
    padding: 15px;
    background-color: #CBAF6E;
}


</style>