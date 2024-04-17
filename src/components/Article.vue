<script>
import PoliticasAfirmativas from '../assets/pa_regular_cand.jpg'
import DisputaPartidaria from '../assets/dp_regular_cand.jpg'
export default {
    data() {
        return {
            article: [
                { 
                    title: 'A Política de Gênero Afirmativa, Compulsória e Necessária em Eleições.', 
                    description: 'É de se reconhecer que a humanidade se constituiu com âmago masculino. Contudo, é fato que a luta das mulheres por igualdade de direito e de condições na sociedade construiu e constrói novas perspectivas. E, não é diferente na Política, já aparecendo mudanças no conjunto de atos normativos de eleições.| As Ações afirmativas surgiram com objetivos de garantir a igualdade de oportunidades e tratamento ou compensar perdas provocadas pela discriminação.| Para eleições, foi com a Lei nº 9.100, de 1995, a qual estabeleceu as normas para as eleições municipais de 1996, que surgiu a Política Afirmativa de obrigar o Partido ou Coligação, ao apresentar candidatos à Vereador, preencher o número de vagas com no mínimo 20% de candidatas mulheres.| A luta permanente das mulheres e das suas representantes no Congresso, já no ano seguinte àquelas eleições, garante que o percentual mínimo passe a ser 30% (com a transição de ser de 25% para as eleições de 1998), no instrumento normatizador do processo eleitoral brasileiro. Portanto, é com a Lei nº 9.504, de 1997, que se tem o fim das promulgadas novas leis em cada eleição, debelando a possibilidade de uma série de casuísmos.| Entretanto, a redação dada ao § 3º, art. 10, da citada lei, mantém o movimento de mulheres na luta e altivo, já que a cota estipulada para seu cumprimento ficava a cargo dos partidos, bastando reservar, proporcionando, assim, a interpretação de que não havendo mulheres candidatas, as vagas estando disponibilizadas cumpriria a legislação ou mesmo, que homens poderiam ocupar a vaga. Levando à justiça a divergência. Se mantendo, por inúmeras decisões judiciais, a interpretação de que a cota é de mulheres.| No entanto, com a minirreforma eleitoral - Lei nº 12.034, de 2009-, o Congresso Nacional estabelece que os partidos "preencherá" e não mais “deverá reservar”, eliminando de vez as dúvidas acerca de sua obrigatoriedade e atribuindo caráter cogente à norma.| Mesmo a legislação estipulando que os percentuais de 70% e 30% não se vinculam a nenhum sexo, aplicando-se, a rigor, a ambos, é inegável que a compulsoriedade destes percentuais objetiva garantir uma maior participação de mulheres no processo eleitoral.| Importante ressalvar que na reserva de vagas por sexo, qualquer fração será igualada a um no cálculo do percentual mínimo para um dos sexos e desprezada no cálculo das vagas restantes para o outro sexo. Mesmo que, em regra, na hipótese de resultado fracionário, o § 4º do art. 10, da Lei das Eleições, estipular que deve ser desprezada a fração, se inferior a meio, e igualada a um, se igual ou superior.| A luta das mulheres ainda conquista o direito de ter 30% das verbas de campanha para as Candidatas, quer seja provenientes do Fundo Partidário ou do Fundo Especial Financiamento de Campanha-FEFC, o conhecido Fundo Eleitoral, e também garantem o mesmo percentual no tempo da propaganda eleitoral gratuita de Rádio e TV.| As conquista estão consolidadas em favor das candidaturas femininas, importante que mais mulheres participem do processo de eleições como candidatas para que a representação parlamentar se consolide no mínimo com o percentual de 30% conquistado.', 
                    image: PoliticasAfirmativas,
                    writer: 'Anselmo Castilho, Advogado - Atualizado em Abril/2024'
                },
                { 
                    title: 'Iniciam-se a Disputa por Representatividade, com as Convenções Partidárias.', 
                    description: 'Próximo dia 20 de julho, estendendo-se até 05 de agosto, inicia-se o período para que os partidos decidam, em convenção, sua tática eleitoral: apresentando candidato a Prefeito ou declarando apoio, passando a integrar coligação, bem como apresentando chapa que disputará a composição das Câmaras Municipais.| Desde do pleito de 2020 não há coligações para as eleições proporcionais, no caso, vereador(a). Regra imposta pela Emenda Constitucional nº 97, de 04 de outubro de 2017.| Destarte, com o fim das coligações, cada partido e federação com anotação no Tribunal Superior Eleitoral - TSE têm direito de lançar até o número de lugares a preencher nas Câmaras de Vereadores, mais um lugar.| Hoje, no Brasil, existem 29 partidos políticos com registro, sendo que sete desses estão federados em 3 federações distintas.| Assim, cabe a cada Partido definir a respectiva data de sua Convenção, evento que delibera acerca da Candidatura Majoritária e formação da Chapa Proporcional, observando o percentual mínimo de 30% (trinta por cento) e o máximo de 70% (setenta por cento) para candidaturas de cada sexo. Regra prevista no art. 10, § 3º, da Lei Geral das Eleições, Lei 9.504, de 1997.', 
                    image: DisputaPartidaria,
                    writer: 'Anselmo Castilho, Advogado - Atualizado em Abril/2024'
                },
            ],
            showFull: [],
            toggleButton : false,
            indexButton: 0
        };
        
    },
    methods: {
        truncateDescription(description) {
            return description.split(' ').slice(0, 27).join(' ') + '...';
        },
        adicionarLinhasVazias(descricao) {
            const frases = descricao.split('|');
            for (let i = 0; i < frases.length - 1; i++) {
                frases[i] += '<br><br>';
            }
            return frases.join('');
        }
}
}
</script>

<template>
<section class="bg-[#DFCCA5] py-20"><!--ARTIGOS-->
    <div class="container">
        <h2 class="text-4xl text-center pb-8">Artigos</h2>
        <div class="grid sm:grid-cols-2 lg:grid-cols-3 px-5 lg:px-0 gap-y-5 lg:gap-y-0 gap-x-6">
            <div v-for="(item, index) in article" :key="index" class="space-y-2">
                <img class="rounded w-full" :src="item.image" alt="">
                <h3 class="font-semibold text-2xl">{{item.title}}</h3>
                <p>{{ truncateDescription(item.description) }}</p>
                <button @click="toggleButton = true; indexButton = index" class="w-1/2 rounded bg-[#BE9C4B] hover:bg-[#967936] transition-colors duration-500 p-3 text-md">{{ showFull[index] ? 'Fechar artigo' : 'Leia o artigo completo' }}</button>
                <div v-if="toggleButton && indexButton == index" class="full-article-overlay">
                    <div class="full-article space-y-2">
                        <svg @click="toggleButton = false" xmlns="http://www.w3.org/2000/svg" width="30" height="30" fill="red" class="close-button bi bi-x-lg" viewBox="0 0 16 16">
                            <path d="M2.146 2.854a.5.5 0 1 1 .708-.708L8 7.293l5.146-5.147a.5.5 0 0 1 .708.708L8.707 8l5.147 5.146a.5.5 0 0 1-.708.708L8 8.707l-5.146 5.147a.5.5 0 0 1-.708-.708L7.293 8z"/>
                        </svg>
                        <h3 class="font-semibold text-2xl">{{ item.title }}</h3>
                        <p v-html="adicionarLinhasVazias(item.description)"></p>
                        <p class="pt-2 font-semibold text-xl">{{ item.writer }} </p>
                    </div>
                </div>
            </div>
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

.full-article-overlay {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.5);
    display: flex;
    justify-content: center;
    align-items: center;
}

.full-article {
    background-color: white;
    border-radius: 6px;
    padding: 20px;
    max-width: 80%;
    max-height: 80%;
    overflow-y: auto;
    position: relative;
}

.close-button {
    position: absolute;
    top: 10px;
    right: 10px;
    background: none;
    border: none;
    cursor: pointer;
    font-size: 24px;
}
</style>