<script>
export default {

    data() {
        return {
            eleitoral_date: [
                { 
                    date: "05/04/2024", 
                    theme: "Desfiliação Partidária", 
                    description: "Último dia do período em que se considera justa causa para a desfiliação partidária de vereadoras e vereadores a mudança de partido para concorrer a cargo de prefeito ou de vereador (Lei nº 9.096/1995, art. 22-A, III)", 
                    clicked: false 
                },
                { 
                    date: "06/04/2024", 
                    theme: "Domicílio Eleitoral e Renúncia de Cargo Vigente", 
                    description: "Data até a qual os que pretendam ser candidatos a cargo eletivo nas eleições de 2024 estejam com DOMICÍLIO ELEITORAL na circunscrição (município) na qual desejam concorrer e estejam com a FILIAÇÃO deferida pelo partido, desde que o estatuto partidário não estabeleça prazo superior (Lei nº 9.504, de 1997, art. 9º, caput e Lei nº 9.096, de 1995, art. 20, caput). Data até a qual as Prefeitas, os Prefeitos devem renunciar aos respectivos mandatos caso pretendam concorrer a outro cargo (CF, art. 14, § 6º).", 
                    clicked: false 
                },
                { 
                    date: "08/04/2024", 
                    theme: "Alistamento, Transferência e Revisão de dados", 
                    description: "Último dia para que eleitoras e eleitores domiciliados(as) no Brasil que não possuem cadastro biométrico na Justiça Eleitoral solicitem operações de alistamento, transferência e revisão pelo serviço de autoatendimento eleitoral na internet", 
                    clicked: false 
                },
                {
                    date: "09/04/2024",
                    theme: "Normas para Escolha e Substituição de Candidatos",
                    description: "Último dia para o órgão de Direção Nacional do Partido Político ou Federação publicar, no Diário Oficial da União, as normas para a escolha e substituição de candidatos e para a formação de coligações (no caso Majoritário), na hipótese de omissão do estatuto (Lei nº 9.504, de 1997, art. 7º, § 1º). Data a partir da qual, até a posse dos eleitos, é vedado ao/à Prefeito/a fazer revisão geral da remuneração dos servidores públicos que exceda a recomposição da perda de seu poder aquisitivo ao longo do ano da eleição (Lei nº 9.504, de 1997, art. 73, VIII).",
                    clicked: false
                },
                {
                    date: "08/05/2024",
                    theme: "Prazo para Inscrição Eleitoral e Regularização",
                    description: "Último dia para o eleitor que pretenda votar nas eleições de 2024 requeira sua inscrição eleitoral, altere seus dados cadastrais ou transfira seu domicílio eleitoral (Lei nº 9.504, de 1997, art. 91, caput). Último dia para o eleitor com deficiência ou mobilidade reduzida solicitar sua transferência para seção com acessibilidade (Lei nº 9.504, de 1997, art. 91, caput). Último dia para que os/as presos/as provisórios e os adolescentes internados que não possuírem inscrição eleitoral regular sejam alistados ou requeiram a regularização de sua situação para votarem nas eleições de 2024.",
                    clicked: false
                },
                {
                    date: "15/05/2024",
                    theme: "Arrecadação Prévia de Recursos para Pré-Candidatos",
                    description: "Data a partir da qual é facultada aos/às pré-candidatos/as a arrecadação prévia de recursos na modalidade de financiamento coletivo (VAQUINHA ELETRÔNICA), ficando a liberação de recursos por parte das entidades arrecadadoras condicionada ao cumprimento, pelo/a candidato/a, do registro de sua candidatura, da obtenção do CNPJ e da abertura de conta bancária (Lei nº 9.504, de 1997, art. 22-A, § 3º). Data a partir da qual é permitida a campanha de arrecadação prévia de recursos na modalidade de financiamento coletivo, observadas a vedação a pedido de voto e as regras relativas à propaganda eleitoral na internet (Lei nº 9.504/1997, art. 22-A, § 3º; e Res.-TSE nº 23.610/2019, art. 3º, § 4º).",
                    clicked: false
                },
                {
                    date: "05/06/2024",
                    theme: "Disponibilização de Devedores de Multa Eleitoral",
                    description: "Data a partir da qual a Justiça Eleitoral deve tornar disponível aos Partidos Políticos a relação de todos os devedores de multa eleitoral, a qual embasará a expedição das certidões de quitação eleitoral (Lei nº 9.504, de 1997, art. 11, § 9º).",
                    clicked: false
                },
                {
                    date: "17/06/2024",
                    theme: "Divulgação do Montante de Recursos do FEFC",
                    description: "Data limite para o Tribunal Superior Eleitoral - TSE divulgar o montante de recursos disponíveis no Fundo Especial de Financiamento de Campanha (FEFC), observados 15 (quinze) dias a partir do recebimento da dotação orçamentária pelo Tribunal (Lei nº 9.504/1997, art. 16-C, § 2º; e Res.-TSE nº 23.605/2019, art. 3º).",
                    clicked: false
                },
                {
                    date: "30/06/2024",
                    theme: "Vedação de Programas Apresentados por Pré-Candidatos",
                    description: "Data a partir da qual é vedado às emissoras de rádio e de televisão transmitir programa apresentado ou comentado por pré-candidata ou pré-candidato (Lei nº 9.504/1997, art. 45, § 1º e Res.-TSE nº 23.610/2019, art. 43, § 2º). Data limite para a prestação de contas anual do Diretório Municipal do Partido (Lei nº 9.096, de 1995, nova redação do art. 32, dada pela Lei nº 13.877, de 2019).",
                    clicked: false
                },
                {
                    date: "05/07/2024",
                    theme: "Período para Propaganda Intrapartidária",
                    description: "Data a partir da qual, observado o prazo de 15 (quinze) dias que antecede a data definida pelo partido para a escolha dos candidatos, é permitido ao postulante à candidatura a cargo eletivo realizar propaganda intrapartidária com vistas à indicação de seu nome, vedado o uso de rádio, televisão e outdoor (Lei nº 9.504, de 1997, art. 8° c/c 36, § 1º).",
                    clicked: false
                },
                {
                    date: "06/07/2024",
                    theme: "Vedação de Condutas para Prefeitos e Agentes Públicos",
                    description: "Data a partir da qual é vedado ao/à Prefeito/a as seguintes condutas (Lei nº 9.504, de 1997, art. 73, incisos V e VI, alínea a): nomear, contratar ou de qualquer forma admitir, demitir sem justa causa, suprimir ou readaptar vantagens ou por outros meios dificultar ou impedir o exercício funcional e, ainda, ex officio, remover, transferir ou exonerar servidor público até a posse do eleito, sob pena de nulidade de pleno direito, ressalvados os casos de: ✓ nomeação ou exoneração de cargos em comissão e designação ou dispensa de funções de confiança; ✓ nomeação dos aprovados em concursos públicos homologados até 6 de julho de 2024; ✓ nomeação ou contratação necessária à instalação ou ao funcionamento inadiável de serviços públicos essenciais, com prévia e expressa autorização do Prefeito; Data a partir da qual é vedado aos agentes públicos das esferas administrativas cujos cargos estejam em disputa na eleição (Lei nº 9.504, de 1997, art. 73, inciso VI, alíneas b e c, e § 3º): ✓ fazer pronunciamento em cadeia de rádio e de televisão, fora do horário eleitoral gratuito, salvo quando, a critério da Justiça Eleitoral, tratar-se de matéria urgente, relevante e característica das funções de governo. Data a partir da qual as(os) agentes públicas(os) devem adotar as providências necessárias para que o conteúdo dos sítios, canais e outros meios de informação oficial exclua nomes, slogans, símbolos, expressões, imagens ou outros elementos que permitam identificar autoridades, governos ou administrações, cujos cargos estejam em disputa na campanha eleitoral, ainda que a divulgação tenha sido autorizada em momento anterior, assegurada a manutenção das informações necessárias para estrito cumprimento, pelos responsáveis, do previsto no art. 48-A da Lei Complementar nº 101/2000, nos arts. 8º e 10 da Lei nº 12.527/2011 e no §2º do art. 29 da Lei nº 14.129/2021. Data a partir da qual é vedada, na realização de inaugurações, a contratação de shows artísticos pagos com recursos públicos (Lei nº 9.504, de 1997, art. 75). Data a partir da qual é proibido a candidata ou candidato comparecer a inaugurações de obras públicas (Lei nº 9.504/1997, art. 77).",
                    clicked: false
                },
                {
                    date: "20/07/2024",
                    theme: "Convenções e Direito de Resposta; Asseguramento de Órgãos de Direção e Federações; Formalização de Contratos; Definição de Limites de Gastos; Divulgação de Recursos Financeiros",
                    description: "Data a partir da qual, até 5 de agosto de 2020, é permitida a realização de convenções destinadas a deliberar sobre coligações e a escolher candidatos/as a Prefeito/a e Vereadores/as (Lei nº 9.504, de 1997, art. 8º,caput). Data a partir da qual é assegurado o exercício do direito de resposta ao/à candidato/a, ao partido político ou à coligação atingidos, ainda que de forma indireta, por conceito, imagem ou afirmação caluniosa, difamatória, injuriosa ou sabidamente inverídica, difundidos por qualquer veículo de comunicação social (Lei nº 9.504/1997, art. 58, caput). Data a partir da qual os partidos políticos e as federações deverão assegurar que, na data da convenção em cada Município: a) o partido político que deseje participar das eleições tenha órgão de direção constituído na circunscrição, devidamente anotado no Tribunal Regional Eleitoral - TRE, de acordo com o respectivo estatuto partidário (Lei nº 9.504/1997, art. 4º; Res.-TSE nº 23.609/2019, art. 2º, I) b) a federação que deseje participar das eleições conte, em sua composição, com ao menos um partido político que tenha órgão de direção que atenda ao disposto no item “a” supra (Lei nº 9.504/1997, arts. 4º e 6º-A; e Res.-TSE nº 23.609/2019, art. 2º, II). Data a partir da qual, considerada o dia seguinte da data da efetiva realização da respectiva convenção partidária, é permitida a formalização de contratos que gerem despesas e gastos com a instalação física e virtual de comitês de candidatos e de partidos políticos, desde que só haja o efetivo desembolso financeiro após a obtenção do número de registro de CNPJ do candidato e a abertura de conta bancária específica para a movimentação financeira de campanha e emissão de recibos eleitorais (Lei nº 9.504/1997, art. 26, VI e Res.-TSE nº 23.607, art. 36 § 2º). Data a partir da qual, observado o dia seguinte ao qual se realizou a convenção, os partidos políticos e as federações deverão transmitir pela internet a ata e a lista das pessoas presentes, digitadas no CANDex ou, na impossibilidade, entregá-las em mídia no cartório eleitoral, para publicação no sítio eletrônico da Justiça Eleitoral (Lei nº 9.504/1997, art. 8º, caput e Res.-TSE nº 23.609, art. 6º §§ 4º, I e 5º). Último dia para o Tribunal Superior Eleitoral publicar portaria com os limites de gastos de campanha estabelecidos em lei paracada cargo eletivo em disputa (Lei nº 9.504/1997, art. 18 ; e Res.-TSEnº 23.607/2019, art. 4º, § 2º). Data em que o Tribunal Superior Eleitoral divulgará, na internet, o quantitativo de eleitoras e eleitores por Município, para fins do cálculo do limite de gastos e do número de contratações diretas ou terceirizadas de pessoal para prestação de serviços referentes a atividades de militância e mobilização de rua nas campanhas eleitorais (Lei nº 9.504/1997, art. 100-A , Lei nº 13.488/2017, art. 6º e Res.-TSE nº 23.607, art. 41, § 4º). Data a partir da qual os partidos políticos, as candidatas e os candidatos deverão enviar à Justiça Eleitoral os dados sobre recursos financeiros recebidos para financiamento de sua campanha eleitoral, observado o prazo de 72 (setenta e duas) horas do recebimento desses recursos, para fins de divulgação na internet (Lei nº 9.504/1997, art. 28, § 4º, I ; e Res.-TSE nº 23.607/2019, art. 47).",
                    clicked: false
                },
                {
                    date: "21/07/2024",
                    theme: "Consulta de Locais de Votação com Vagas Especiais",
                    description: "Data a partir da qual será disponibilizada, na internet, consulta dos locais de votação com vagas para a transferência temporária de seção para militares, agentes de segurança pública, guardas municipais, juízas e juízes eleitorais, juízas e juízes auxiliares, servidoras e servidores da Justiça Eleitoral e promotoras e promotores eleitorais em serviço no dia das eleições.",
                    clicked: false
                },
                {
                    date: "22/07/2024",
                    theme: "Habilitação para Votação em Outra Seção ou Local",
                    description: "Data a partir da qual e até 22 de agosto de 2024, poderão habilitar-se, na Justiça Eleitoral, para votar em outra seção ou local, dentro do mesmo Município onde estão inscritas(os): a) presas e presos provisórias(os) e adolescentes em unidades de internação, mediante formulário próprio encaminhado pela administração dos estabelecimentos penais e das unidades de internação de adolescentes; b) militares, agentes de segurança pública e guardas municipais em serviço no dia da eleição, mediante listagem encaminhada pela chefia ou comando do órgão aos quais estiverem subordinadas; c) pessoas com deficiência ou com mobilidade reduzida; d) indígenas, quilombolas, integrantes de comunidades tradicionais e residentes de assentamentos rurais; e) juízas e juízes eleitorais, juízas e juízes auxiliares, servidoras e servidores da Justiça Eleitoral e promotoras e promotores eleitorais em serviço no dia das eleições, mediante listagem encaminhada pelo órgão ou unidade a que estiver vinculada(o) a eleitora ou o eleitor. Data a partir da qual e até 30 de agosto de 2024, poderá habilitar-se na Justiça Eleitoral para votar, desde que no mesmo Município da sua inscrição eleitoral: a) a mesária ou o mesário, na seção em que atuará; b) a(o) convocada(o) para prestar apoio logístico, no local onde atuará; c) a(o) nomeada(o) para atuar nos testes de integridade das urnas eletrônicas, em local próximo ao evento; d) a(o) agente penitenciária(o), a(o) policial penal, a servidora ou o servidor de estabelecimentos penal ou de unidade de internação de adolescentes custodiadas(os), se estiver em serviço, na seção eleitoral do local, se for instalada.",
                    clicked: false
                },
                {
                    date: "26/07/2024",
                    theme: "Publicação de Composição de Juntas Eleitorais",
                    description: "Último dia para a publicação do edital com os nomes das pessoas indicadas para compor as juntas eleitorais para o primeiro e eventual segundo turnos de votação, contando-se da data da publicação o prazo de 3 (três) dias para que partidos políticos e federações apresentem impugnação (Código Eleitoral, art. 36, § 2º).",
                    clicked: false
                },
                {
                    date: "04/08/2024",
                    theme: "Período de Propaganda Intrapartidária",
                    description: "Data até a qual, respeitado o período de 15 (quinze) dias que antecede a convenção do partido político ou da federação para escolha de candidatas e candidatos, é permitida a realização de propaganda intrapartidária, com vista à indicação de nomes para concorrer aos cargos de prefeito, vice-prefeito e vereador, vedado o uso de rádio, televisão e outdoor e devendo a propaganda ser removida imediatamente após a convenção (Lei nº 9.504/1997, art. 36, § 1º e Res.-TSE nº 23.610/2019, art. 2º, § 1º).",
                    clicked: false
                },
                {
                    date: "05/08/2024",
                    theme: "Último Dia para Convenções",
                    description: "Último dia para a realização de convenções destinadas a deliberar sobre coligações para eleição majoritária e escolher o candidato a Prefeito/a e deliberar acerca da chapa de vereadores/as (Lei nº 9.504, de 1997, art. 8º, caput).",
                    clicked: false
                },
                {
                    date: "07/08/2024",
                    theme: "",
                    description: "Último dia para o eleitor que estiver fora do seu domicílio eleitoral requerer a segunda via do título eleitoral em qualquer cartório eleitoral, esclarecendo se vai recebê-la na sua zona eleitoral ou naquela em que a requereu (Código Eleitoral, art. 53, § 4º). Data a partir da qual é assegurada aos partidos políticos e às federações a prioridade postal para a remessa de material de propaganda de suas candidatas e de seus candidatos (Código Eleitoral, art. 239; e Res.-TSE nº 23.610/2019, art. 120). Último dia para publicação de edital com os locais designados para o funcionamento das Mesas Receptoras de Votos e de Justificativa, incluídas as agregadas, com a numeração ordinal e o local em que deverão funcionar, assim como a indicação da rua, do número e de qualquer outro elemento que facilite a sua localização, contandose da publicação do edital o prazo de 3(três) dias para que os partidos políticos e as federações reclamem da designação (Código Eleitoral 135, caput e §§ 1º e 7º).",
                    clicked: false
                },
                {
                    date: "13/08/2024",
                    theme: "Último Dia para Requerimento de Segunda Via e Publicação de Locais de Votação",
                    description: "Data-limite para que o Tribunal Superior Eleitoral publique a tabela com a representação dos partidos políticos na Câmara dos Deputados e no Congresso Nacional, consideradas as novas totalizações do resultado das últimas eleições gerais que ocorrerem até 20 de julho de 2024, para divisão do tempo destinado à propaganda eleitoral gratuita no rádio e na televisão e para a realização de debates (Res.-TSE nº 23.610/2019, arts. 44, § 6º e 55, I).",
                    clicked: false
                },
                {
                    date: "15/08/2024",
                    theme: "Prioridade Postal e Abertura de Conta Bancária",
                    description: "Último dia para os partidos políticos e as coligações apresentarem a Justiça Eleitoral o requerimento de registro de candidatos a Prefeito/a e a Vereadores/as (Lei nº 9.504, de 1997, art. 11, caput e Res.-TSE nº 23.609/2019, arts. 18, III e 19, § 2º): a) até as 8h (oito horas), por transmissão via internet; ou b) até as 19h (dezenove) horas, em mídia entregue nos cartórios eleitorais. Data a partir da qual permanecerão abertas aos sábados, domingos e feriados as secretarias das Zonas Eleitorais, devendo os prazos processuais relativos aos feitos eleitorais serem contínuos e peremptórios (Lei Complementar nº 64, de 1990, art. 16). Data limite para que os partidos providenciem a abertura de conta bancária específica destinada à movimentação de recursos públicos e privados para a campanha eleitoral, na Caixa Econômica Federal, no Banco do Brasil ou em outra instituição financeira com carteira comercial reconhecida pelo Banco Central do Brasil (Res.-TSE nº 23.607/2019, art. 8º,§ 1º, II). Último dia para os partidos políticos encaminharem ao Tribunal Superior Eleitoral os critérios definidos pelos órgãos de direção nacional para utilização, nas campanhas eleitorais, das doações recebidas de pessoas físicas ou das contribuições de filiadas e filiados recebidas em anos anteriores ao da eleição (Res.-TSE nº 23.607/2019, art. 18, II).",
                    clicked: false
                },
                {
                    date: "16/08/2024",
                    theme: "Início da Propaganda Eleitoral",
                    description: "Data a partir da qual será permitida a propaganda eleitoral (Lei nº 9.504/1997, art. 36, caput e 57-A e Res.-TSE nº 23.610/2019, arts. 2º e 27)",
                    clicked: false
                },
                {
                    date: "17/08/2024",
                    theme: "Publicação de Oferta de Transporte",
                    description: "Data-limite para que o poder público informe ao juízo eleitoral itinerários, horários e modalidades de transporte que irá ofertar gratuitamente nos dias de votação.",
                    clicked: false
                },
                {
                    date: "20/08/2024",
                    theme: "Divulgação de Percentuais de Candidaturas e Último Dia para Registro",
                    description: "Data-limite para que o Tribunal Superior Eleitoral divulgue em sua página da internet os percentuais de candidaturas de femininas e de pessoas negras por partido político, calculados sobre o total de candidaturas que constaram de pedidos coletivos (RRC) e individuais (RRCI) no território nacional, para a destinação dos recursos do fundo partidário e do FEFC, de acordo com as reservas estabelecidas no § 4º do art. 17 e no § 3º do art. 19 da Resolução TSE nº 23.607 de 2019. Último dia, observado o prazo de 48 h (quarenta e oito horas) contadas da publicação do edital de candidaturas requeridas, para os candidatos escolhidos em convenção solicitarem seus registros na Justiça Eleitoral, até 19 horas, caso os partidos políticos ou as coligações não os tenham requerido (Lei nº 9.504, de 1997, art. 11, § 4º).",
                    clicked: false
                },
                {
                    date: "22/08/2024",
                    theme: "Prazo Final para Habilitação e Impugnação",
                    description: "Último dia, observado o prazo de 5 (cinco) dias contados da publicação do edital de candidaturas requeridas, para qualquer candidato, partido político, coligação ou o Ministério Público impugnar os pedidos de registro de candidatos apresentados pelos partidos políticos ou coligações (Lei Complementar nº 64/1990, art. 3º). Último dia, observado o prazo de 5 (cinco) dias contados da publicação do edital de candidaturas requeridas, para qualquer cidadão no gozo de seus direitos políticos dar ao juízo eleitoral notícia de inelegibilidade que recaia em candidato com pedido de registro apresentado pelo partido político ou pela coligação.",
                    clicked: false
                },
                {
                    date: "25/08/2024",
                    theme: "Reunião para Elaboração de Plano de Mídia",
                    description: "Data-limite para que as juízas ou os juízes eleitorais responsáveis pela propaganda convoquem os partidos políticos, as federações e a representação das emissoras de televisão e de rádio para a elaboração de plano de mídia para uso da parcela do horário eleitoral gratuito a que tenham direito e para realizar o sorteio para escolha da ordem de veiculação da propaganda em rede (Lei nº 9.504/1997, art. 52 e Res.-TSE nº 23.610/2019, arts. 53, caput e § 1º).",
                    clicked: false
                },
                {
                    date: "27/08/2024",
                    theme: "Indicação de Comissão Especial de Transporte",
                    description: "Último dia para os partidos políticos e federações indicarem até 3 (três) pessoas para compor a Comissão Especial de Transporte para o primeiro e eventual segundo turnos de votação (Lei nº 6.091, art. 14, § 1º e art. 15; e Res.- TSE nº 9.641/1974, art. 13, §§ 1º e 3º).",
                    clicked: false
                },
                {
                    date: "28/08/2024",
                    theme: "Indicação de Pessoas Autorizadas e Fornecimento de Contatos",
                    description: "Último dia para os partidos, as federações e as coligações indicarem ao grupo de emissoras ou à emissora responsável pela geração do sinal para veiculação da propaganda eleitoral gratuita, as pessoas autorizadas a entregar os mapas e as mídias, comunicando eventual substituição com, no mínimo, 24 (vinte e quatro) horas de antecedência, dispensado o credenciamento para as(os) presidentes das legendas e as(os) vice-presidentes e delegadas(os) credenciadas(os), mediante certidão obtida no sítio eletrônico do TSE (Res.-TSE nº 23.610/2019, art. 65, §§ 1º e 3º). Último dia para o grupo de emissoras e as emissoras responsáveis pela geração fornecerem à Justiça Eleitoral, aos partidos políticos, às federações e às coligações, por formulário estabelecido no Anexo II da Res.- TSE nº 23.610/2019, seus telefones, endereços, inclusive eletrônico, e nomes das pessoas responsáveis pelo recebimento de mapas e de mídias (Res.-TSE nº23.610/2019, art. 65, § 8º).",
                    clicked: false
                },
                {
                    date: "30/08/2024",
                    theme: "Início da Propaganda Eleitoral Gratuita e Distribuição de Recursos",
                    description: "Início do período da propaganda eleitoral gratuita no rádio e na televisão (Lei nº 9.504, de 1997, art. 47, caput). Último dia para os partidos efetuarem a distribuição dos recursos públicos do Fundo Especial de Financiamento de Campanha e do Fundo Partidário às candidaturas femininas e de pessoas negras (Res.-TSE nº 23.607/2019, arts. 17, § 10, e 19, § 10).",
                    clicked: false
                },
                {
                    date: "03/09/2024",
                    theme: "Consulta de Seção de Votação",
                    description: "Data a partir da qual estará disponível, no e-Título ou na internet, o serviço de consulta à seção de votação, atualizada com as informações a respeito da transferência temporária da eleitora ou do eleitor.",
                    clicked: false
                },
                {
                    date: "06/09/2024",
                    theme: "",
                    description: "Último dia para os órgãos de direção dos partidos políticos preencherem as vagas remanescentes para as eleições proporcionais, observados os percentuais mínimo e máximo para candidaturas de cada sexo, no caso de as convenções para a escolha de candidatos/as não terem indicado o número máximo previsto no caput do art. 10 da Lei nº 9.504, de 1997 (§ 5º, art. 10, Lei nº 9.504, de 1997 e Res.TSE nº 23.609/2019, art. 17, § 7º)",
                    clicked: false
                },
                {
                    date: "09/09/2024",
                    theme: "Envio de Prestação Parcial de Contas",
                    description: "Data a partir da qual e até 13 de setembro de 2024, os partidos políticos, as candidatas e os candidatos deverão enviar à Justiça Eleitoral, pelo Sistema de Prestação de Contas Eleitorais (SPCE), a prestação parcial de contas, dela constando o registro da movimentação financeira e/ou estimável em dinheiro ocorrida desde o início da campanha até 8 de setembro de 2024, para cumprimento do disposto no inciso II do § 4º do art. 28 da Lei nº 9.504 de 1997 (Res.TSE nº 23.607/2019, art. 47, § 4º).",
                    clicked: false
                },
                {
                    date: "13/09/2024",
                    theme: "Prazo Final para Envio de Prestação Parcial de Contas",
                    description: "Último dia para que os partidos políticos, as candidatas e os candidatos enviem à Justiça Eleitoral, pelo Sistema de Prestação de Contas Eleitorais (SPCE), a prestação parcial de contas, dela constando o registro da movimentação financeira e/ou estimável em dinheiro ocorrida desde o início da campanha até 8 de setembro de 2024, para cumprimento do disposto no inciso II do § 4º do art. 28 da Lei nº 9.504 de 1997 (Res.-TSE nº 23.607/2019, art. 47, § 4º).",
                    clicked: false
                },
                {
                    date: "14/09/2024",
                    theme: "Comunicação de Anulações de Deliberações",
                    description: "Último dia para os partidos políticos, as federações e as coligações comunicarem à Justiça Eleitoral anulações de deliberações dos atos decorrentes de convenção partidária, observado, quanto à escolha de novas(os) candidatas(os), a necessidade de o pedido de registro ser apresentado à Justiça Eleitoral nos 10 (dez) dias seguintes à deliberação (Lei nº 9.504/1997, art. 7º, §§ 3º e 4º; e Res.TSE nº 23.609/2019, art. 8º, § 1º).",
                    clicked: false
                },
                {
                    date: "15/09/2024",
                    theme: "Divulgação da Prestação de Contas Parcial",
                    description: "Data em que será divulgada, pela internet, em sítio criado pela Justiça Eleitoral para esse fim, a prestação de contas parcial, dela constando o registro da movimentação financeira e/ou estimável em dinheiro ocorrida desde o início da campanha até o dia 8 de setembro do mesmo ano, observadas as diretrizes para tratamento de dados pessoais da Lei nº 13.709 de 2018 e da Resolução TSE nº 23.650 de 2021 (Lei nº 9.504/1997, art. 28, § 4º, II; e Res.TSE nº 23.607/2019, art. 47, § 5º).",
                    clicked: false
                },
                {
                    date: "16/09/2024",
                    theme: "Julgamento de Pedidos de Registro de Candidaturas",
                    description: "Data em que todos os pedidos de registro de candidaturas aos cargos de prefeito, vice-prefeito e vereador, inclusive os impugnados e os respectivos recursos, devem estar julgados pelas instâncias ordinárias e publicadas as decisões (Lei nº9.504/1997, art. 16, § 1º e Res.-TSE nº 23.609/2019, art. 54).\nÚltimo dia para o pedido de substituição de candidatas ou de candidatos para os cargos majoritários e proporcionais, exceto se a substituição decorrer de falecimento, caso em que poderá ser efetivado após esta data, observado, em qualquer situação, o prazo de até 10 (dez) dias contados do fato, inclusive anulação de convenção, ou da decisão judicial que deu origem à substituição (Lei nº 9.504/1997, arts. 7º, § 4º, e 13, §§ 1º e 3º; e Res.TSE nº 23.609/2019, art. 72 § 3º).",
                    clicked: false
                },
                {
                    date: "21/09/2024",
                    theme: "Início da Proibição de Prisões de Candidatos",
                    description: "Data a partir da qual e até 8 de outubro, nenhuma candidata ou candidato poderá ser detida(o) ou presa(o), salvo em flagrante delito (Código Eleitoral, art. 236, § 1º).\nData em que deverá ser divulgado o quadro geral de percursos e horários programados para o transporte de eleitoras e de eleitores para o primeiro e eventual segundo turnos de votação, contando-se da divulgação o prazo de 3 (três) dias para que os partidos políticos, as federações, as candidatas, os candidatos, as eleitoras e os eleitores apresentem reclamação (Lei nº6.091/1974, art. 4º).",
                    clicked: false
                },
                {
                    date: "26/09/2024",
                    theme: "Prazo para Requerimento de Segunda Via do Título Eleitoral",
                    description: "Último dia para o eleitor requerer a segunda via do título eleitoral dentro do seu domicílio eleitoral (Código Eleitoral, art. 52)",
                    clicked: false
                },
                {
                    date: "01/10/2024",
                    theme: "Início da Proibição de Prisões de Eleitores",
                    description: "Data a partir da qual nenhum eleitor poderá ser preso ou detido, salvo em flagrante delito, ou em virtude de sentença criminal condenatória por crime inafiançável, ou por desrespeito a salvo-conduto (Código Eleitoral, art. 236, caput).",
                    clicked: false
                },
                {
                    date: "03/10/2024",
                    theme: "Último Dia para Divulgação de Propaganda Eleitoral",
                    description: "Último dia para a divulgação da propaganda eleitoral gratuita no rádio e na televisão (Lei nº 9.504, de 1997, art. 47, caput).\nÚltimo dia para propaganda política mediante reuniões públicas ou promoção de comícios e utilização de aparelhagem de sonorização fixa, entre as 8 e as 24 horas, com exceção do comício de encerramento da campanha, que poderá ser prorrogado por mais 2 (duas) horas (Código Eleitoral, art. 240, parágrafo único, e Lei nº 9.504, de 1997, art. 39, §§ 4º e 5º, inciso I).\nÚltimo dia para a realização de comícios e utilização de aparelhagem de sonorização fixa, entre as 8h (oito horas) e as 24h (vinte e quatro horas), com exceção do comício de encerramento da campanha, que poderá ser prorrogado por mais 2 (duas) horas (Código Eleitoral, art. 240, parágrafo único; Lei nº 9.504/1997, art. 39, § 4º; e Res.-TSE nº 23.610/2019, arts. 5º e 15, § 1º).\nÚltimo dia para a realização de debate no rádio e na televisão, admitida sua extensão até as 7h (sete horas) do dia 4 de outubro (Res.TSE nº 23.610/2019 art. 46, IV).",
                    clicked: false
                },
                {
                    date: "04/10/2024",
                    theme: "Comunicação de Fiscais e Delegados de Votação",
                    description: "Último dia para a(o) presidente do partido político ou da federação, a(o) representante da coligação ou outra pessoa por elas(eles) indicada comunicarem aos juízos eleitorais os nomes das pessoas autorizadas a expedir as credenciais das(os) fiscais e das(os) delegadas(os) habilitadas(os) a fiscalizar os trabalhos de votação, apuração e totalização do primeiro turno das eleições (Lei nº 9.504/1997, art. 65, § 3º).\nÚltimo dia para a(o) presidente do partido político ou da federação, a(o) representante da coligação ou outra pessoa por elas(eles) indicada comunicarem aos juízos eleitorais os nomes das pessoas autorizadas a fiscalizar os trabalhos de votação do primeiro turno nas seções eleitorais instaladas nos estabelecimentos penais e de internação de adolescentes (Lei nº 9.504/1997, art. 65, § 3º).\nÚltimo dia para a divulgação paga, na imprensa escrita, de propaganda eleitoral e a reprodução, na internet, de jornal impresso com propaganda eleitoral (Lei nº 9.504, de 1997, art. 43 e Res.TSE nº 23.610/2019, art. 42).\nÚltimo dia para a circulação paga ou impulsionada de propaganda eleitoral na internet, mesmo se a contratação tiver sido realizada antes desse prazo, cabendo ao provedor de aplicação, que comercializa o impulsionamento, realizar o desligamento da veiculação de propaganda eleitoral (Res.TSE nº 23.610/2019, art. 29, § 11).",
                    clicked: false
                },
                {
                    date: "05/10/2024",
                    theme: "Último Dia para Propaganda com Alto-Falantes e Material Gráfico",
                    description: "Último dia para a propaganda eleitoral mediante altofalantes ou amplificadores de som, entre as 8 e as 22 horas (Lei nº 9.504, de 1997, art. 39, §§ 3º e 5º, inciso I e Res. TSE nº 23.610/2019, art. 15).\nÚltimo dia, até as 22 horas, para a distribuição de material gráfico e a promoção de caminhada, carreata, passeata ou carro de som que transite pela cidade divulgando jingles ou mensagens de candidatos (Lei nº 9.504, de 1997, art. 39, § 9º e Res.TSE nº 23.610/2019, art. 16).",
                    clicked: false
                },
                {
                    date: "06/10/2024",
                    theme: "Dia das Eleições (1º Turno)",
                    description: "DIA DAS ELEIÇÕES (1º turno)\n(Constituição Federal, arts. 14, caput e 29, I e II; Código Eleitoral, art. 82; Lei nº 9.504/1997, art. 1º, parágrafo único, II, e art. 3º).",
                    clicked: false
                }
            ],
            selectedItem: null,
        };
    },
    methods: {
        toggleClicked(index) {
            const clickedItem = this.eleitoral_date[index];
            if (!clickedItem.clicked) {
                this.eleitoral_date.forEach((item, i) => {
                    item.clicked = i === index;
                });
                this.selectedItem = clickedItem;
            }
        },
        getIconColor(date, index) {
            const currentDate = new Date();
            const [day, month, year] = date.split('/');
            const eventDate = new Date(year, month - 1, day);

            if (eventDate > currentDate && !this.firstAvailableDateFound || eventDate > currentDate && this.IndexOfFirstDateAvailable === index) {
                this.firstAvailableDateFound = true;
                console.log(this.firstAvailableDateFound)
                return '#0A014F'; 
            } else if (eventDate > currentDate) {
                return '#3A7D44'; 
            } else {
                return '#D00000'; 
            }
            }
    },
    created() {
        for (let i = 0; i < this.eleitoral_date.length; i++) {
        const { date } = this.eleitoral_date[i];
        const [day, month, year] = date.split('/');
        const eventDate = new Date(year, month - 1, day);
        
        if (eventDate > new Date()) {
            this.selectedItem = this.eleitoral_date[i];
            this.IndexOfFirstDateAvailable = i
            console.log(this.IndexOfFirstDateAvailable)
            this.selectedItem.clicked = true;
            this.firstAvailableDateFound = true;
            break;
        }
    }
}
}
</script>

<template>
<section class="px-5 lg:p-20 pb-2">
    <div class="container">
        <h2 class="text-4xl text-center pb-8">Datas Eleitorais</h2>
        <div class="grid grid-cols-3 sm:grid-cols-5 lg:grid-cols-10 gap-x-2 gap-y-2">
            <div v-for="(item, index) in eleitoral_date" :key="index" @click="toggleClicked(index)" :class="{ 'border-[#4B3B1B] border-2': item.clicked }" class="bg-[#DFCCA5] cursor-pointer text-center pt-2 space-y-2">
                <div class="justify-center items-center flex">
                    <svg xmlns="http://www.w3.org/2000/svg" width="40" height="40" :fill="getIconColor(item.date, index)" class="bi bi-calendar-event-fill" viewBox="0 0 16 16">
                        <path d="M4 .5a.5.5 0 0 0-1 0V1H2a2 2 0 0 0-2 2v1h16V3a2 2 0 0 0-2-2h-1V.5a.5.5 0 0 0-1 0V1H4zM16 14V5H0v9a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2m-3.5-7h1a.5.5 0 0 1 .5.5v1a.5.5 0 0 1-.5.5h-1a.5.5 0 0 1-.5-.5v-1a.5.5 0 0 1 .5-.5"/>
                    </svg>
                </div>
                <h4 class="text-[#4B3B1B] font-semibold">{{item.date}}</h4>
            </div>
        </div>
        <div v-if="selectedItem" class="mt-10 p-5 bg-[#DFCCA5] space-y-2 rounded text-xl">
            <p><b class="font-semibold text-[#5A4920]">Tema</b>: {{ selectedItem.theme }}</p>
            <p><b class="font-semibold text-[#5A4920]">Data</b>: {{ selectedItem.date }}</p>
            <p><b class="font-semibold text-[#5A4920]">Descrição</b>: {{ selectedItem.description }}</p>
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