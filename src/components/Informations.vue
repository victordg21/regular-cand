<script>
import SVG_1 from '../assets/1-circle-fill.svg'
import SVG_2 from '../assets/2-circle-fill.svg'
import SVG_3 from '../assets/3-circle-fill.svg'
import SVG_4 from '../assets/4-circle-fill.svg'
export default {
    data() {
        return {
            informations: [
                {svg: SVG_1, title: 'Pré-Candidatura', text: 'Constitui-se no registro de todos os dados exigíveis ao cidadão elegível, tendo a finalidade de submissão da sua decisão de candidatura ao respectivo partido ao qual está filiado. O cidadão elegível passará a se beneficiar do RegularCand quando lhe for disponibilizado uma senha de acesso, lhe cabendo responder  os elementos do formulário a fim de possibilitar a interação com os outros ambientes do RegularCand e os profissionais envolvidos na prestação do serviço.'},
                {svg: SVG_2, title: 'Candidatura', text: 'Firma-se a partir do registro da ATA DA CONVENÇÃO PARTIDÁRIA na Justiça Eleitoral. Cabendo à assessoria jurídica anexar no RegularCand a respectiva ata e as certidões criminais; à assessoria contábil anexar o CNPJ da Candidatura, bem como disponibilizar o RAC; e, ao (à) candidato (a) anexar os documentos nos respectivos espaços disponibilizados na ferramenta.'},
                {svg: SVG_3, title: 'Normatização', text: 'Neste ambiente será fornecida a PROCURAÇÃO a ser assinada e anexada pelo (a) candidato (a) em espaço próprio da ferramenta e disponibilizado uma cartilha de orientações eleitoral, acompanhada  de todo o arcabouço legal, bem como ofertado modelos de contratos de prestação de serviços para dawnload, necessários ao pronto atendimento das exigências legais.'},
                {svg: SVG_4, title: 'Prestação de Contas', text: 'Espaço reservado a interação do (a) candidato (a) com a assessoria contábil. A assessoria contábil disponibilizará o CNPJ de candidato (a) e o RAC - Requerimento de Abertura Bancária, a fim do candidato (a) ir ao banco de sua escolha abrir as contas de campanha. De posse dos dados bancários, o (a) candidato (a) informará no espaço reservado do RegularCand, passando, a partir deste momento, a anexar em campo próprio as comprovações de doações recebidas e as notas ficais e recibos das despesas efetivadas.'}
            ]
        };
    },
}
</script>

<template>
    <section class="bg-[#DFCCA5] px-5 lg:px-0 py-20"><!--INFORMAÇÕES-->
        <div class="container">
            <h2 class="text-4xl text-center pb-12">Nossos Serviços</h2>
            <div v-for="(informations, index) in informations" :key="index" class="grid lg:grid-cols-5 px-5 lg:px-0 gap-x-20 py-5">
                <div class="pb-5 sm:pb-0 flex items-center justify-center">
                    <img :src=" informations.svg " alt="">
                </div>
                <div class="lg:col-span-4">
                    <p class="text-lg"><b class="font-semibold text-xl text-[#5A4920]">{{ informations.title }}</b>: {{ informations.text }}</p>
                    
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

</style>