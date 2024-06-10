<script>
export default {
    data() {
        return {
            contact: [
                { information: 'Endereço', answer: 'Avenida Bahia, 761 - 58030-130, João Pessoa, PB'},
                { information: 'Telefone/Whatsapp', answer: '(83) 99981-2066'},
                { information: 'E-mail', answer: 'regularcand2024@gmail.com | castilhoeadv@gmail.com'},
                
            ]
        };
    },
}
</script>

<template>
<section class="bg-[#DFCCA5] px-5 lg:px-0 py-20"><!--CONTATO-->
    <div class="container">
        <h2 class="text-4xl text-center pb-8">Contato</h2>
        <div class="grid grid-cols-1 lg:grid-cols-2 gap-x-20">
            <ul class="space-y-6 pb-5 lg:pb-0">
                <li v-for="(contact, index) in contact" :key="index">
                    <h3 class="text-[#5A4920] font-semibold text-xl pb-2">{{contact.information}}</h3>
                    <p>{{contact.answer}}</p>
                </li>
                <li>
                    <h3 class="text-[#5A4920] font-semibold text-xl pb-2">Horário de Funcionamento</h3>
                    <p>Segunda á Sexta - 8:00 ás 17:00 <br>Sábado - 8:00 ás 13:00</p>
                </li>
            </ul>
            <div>
                <p class="text-xl pt-10 pb-2">Manter contato com nosso serviço é essencial para que possamos atender às suas necessidades de forma eficaz. Seu feedback nos permite ajustar nosso site de acordo com suas preferências, garantindo uma experiência personalizada e satisfatória. Valorizamos suas contribuições e estamos comprometidos em evoluir continuamente para melhor servi-lo. Seu envolvimento é crucial para aprimorarmos nossos serviços e tornar sua interação conosco a melhor possível.</p>
                <a target="_blank" href="https://api.whatsapp.com/send/?phone=558399812066&text&type=phone_number&app_absent=0" class="cursor-pointer rounded bg-[#BE9C4B] hover:bg-[#967936] transition-colors w-full inline-block text-center duration-500 p-3 text-xl">Solicite já seu orçamento</a>
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