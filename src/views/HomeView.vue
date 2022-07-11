<template>
  <main class="py-4">
    <section-image />
    <section-steps
      title="Чекори за купување возило на лизинг:"
      :steps="stepsToBuy"
    />
    <section-documentation
      title="Документација со барање за лизинг: ФИЗИЧКИ ЛИЦА:"
      :documents="documentationPhysical"
    />
    <section-documentation
      title="Документација со барање за лизинг: ПРАВНИ ЛИЦА:"
      :documents="documentationLegal"
    />
    <section-warning />
  </main>
</template>

<script>
import SectionSteps from "../components/SectionSteps.vue";
import SectionImage from "../components/SectionImage.vue";
import SectionWarning from "../components/SectionWarning.vue";
import SectionDocumentation from "../components/SectionDocumentation.vue";
export default {
  name: "HomeView",
  components: {
    SectionSteps,
    SectionImage,
    SectionWarning,
    SectionDocumentation,
  },
  data() {
    return {
      stepsToBuy: [
        {
          title: "ИЗБЕРЕТЕ ГО ВОЗИЛОТО",
          description:
            "Најпрво го избирате возилото кое сакате да го купите и добивате понуда за истото. Според изборот и понудата се подготвуваат потребните документи.",
          description2: "",
        },
        {
          title: "НАШИТЕ ВРАБОТЕНИ ЌЕ ВИ ГИ ПОБАРААТ ПОТРЕБНИТЕ ПОДАТОЦИ",
          description:
            "Ги оставате сите потребни податоци на нашите вработени за да ја подготват целокупната документација која е потребна за аплицирање за лизингот. ",
          description2: "",
        },
        {
          title: "ПРЕДОДОБРУВАЊЕ",
          description:
            "Според податоците се преминува на фазата за пред-одобрување која ги елиминира или намалува можностите да бидете одбиени. Затоа е потребно податоците кои ќе ги оставите да бидат точни и прецизни.Лизинг копманијата ја разгледаува вашата апликација и дололку се е во ред ќе Ви го одобрат лизингот и ќе ве известат за тоа. Дополнително ќе ви ги кажат понатамошните чекори.",
          description2: "",
        },
        {
          title: "КАПАР",
          description:
            "Доколку помине постапката на пред-одобрување потребно е да оставите капар за избраното возило за да Ви биде резервирано се до конечно одобрувањето од банката.",
          description2: "",
        },
        {
          title: "ПРЕЗЕМАЊЕ НА ВОЗИЛОТО",
          description:
            "Откако ќе се завршите целата процедура и лизингот ќе биде одобрен се договара датумот за превземање на возилото.",
          description2:
            "НАПОМЕНА: Пред превземање на возилото потребно е да обезбедите КАСКО ПОЛИСА.",
        },
      ],
      documentationPhysical: [
        {
          description: "ПРОФАКТУРА",
          linkedText: "(превземи барање)",
          link: "https://s-leasing.mk/content/%D0%91%D0%B0%D1%80%D0%B0%D1%9A%D0%B5%20%D0%B7%D0%B0%20%D0%BE%D0%B4%D0%BE%D0%B1%D1%80%D1%83%D0%B2%D0%B0%D1%9A%D0%B5%20%D0%BD%D0%B0%20%D0%BB%D0%B8%D0%B7%D0%B8%D0%BD%D0%B3-Fizicki%20Lica.pdf",
        },
        {
          description: "Копија од ЛИЧНА КАРТА",
        },
        {
          description: "ПОТВРДА од работодавецот за редовен работен однос",
        },
        {
          description: "Административна забрана од плата од работодавецот",
          linkedText: "(превземи Административна забрана)",
          link: "https://s-leasing.mk/content/%D0%90%D0%B4%D0%BC%D0%B8%D0%BD%D0%B8%D1%81%D1%82%D1%80%D0%B0%D1%82%D0%B8%D0%B2%D0%BD%D0%B0%20%D0%B7%D0%B0%D0%B1%D1%80%D0%B0%D0%BD%D0%B0%20%D0%BE%D0%B4%20%D0%BF%D0%BB%D0%B0%D1%82%D0%B0%20%D0%BE%D0%B4%20%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%BE%D0%B4%D0%B0%D0%B2%D0%B5%D1%86%D0%BE%D1%82%20%D0%B2%D0%BE%20%D0%BA%D0%BE%D1%80%D0%B8%D1%81%D1%82%20%D0%BD%D0%B0%20%D0%A8%D0%9F%D0%90%D0%A0%D0%9A%D0%90%D0%A1%D0%95%20%D0%9B%D0%98%D0%97%D0%98%D0%9D%D0%93%20%D0%94%D0%9E%D0%9E%20%D0%A1%D0%BA%D0%BE%D0%BF%D1%98%D0%B5.pdf",
        },
        {
          description: "ИЗЈАВА за редовна отплата",
          linkedText: "(превземи Изјава)",
          link: "https://s-leasing.mk/content/%D0%98%D0%B7%D1%98%D0%B0%D0%B2%D0%B0%20%D0%B7%D0%B0%20%D1%80%D0%B5%D0%B4%D0%BE%D0%B2%D0%BD%D0%B0%20%D0%BE%D1%82%D0%BF%D0%BB%D0%B0%D1%82%D0%B0.pdf",
        },
        {
          description:
            "Годишна даночна пријава (доколку барателот остварува дополнителни приходи)",
        },
        {
          description:
            "Декларации за прием за бруто плата за последните 3 месеци",
        },
        {
          description: "СОГЛАСНОСТ за извадок од Македонско Кредитно Биро",
          linkedText: "(превземи согласност)",
          link: "https://s-leasing.mk/content/%D0%A1%D0%BE%D0%B3%D0%BB%D0%B0%D1%81%D0%BD%D0%BE%D1%81%D1%82%20%D0%B7%D0%B0%20%D0%B8%D0%B7%D0%B2%D0%B0%D0%B4%D0%BE%D0%BA%20%D0%BE%D0%B4%20%D0%9C%D0%B0%D0%BA%D0%B5%D0%B4%D0%BE%D0%BD%D1%81%D0%BA%D0%BE%20%D0%9A%D1%80%D0%B5%D0%B4%D0%B8%D1%82%D0%BD%D0%BE%20%D0%91%D0%B8%D1%80%D0%BE.pdf",
        },
      ],
      documentationLegal: [
        {
          description: "Барање за одобрување на лизинг",
          linkedText: "(превземи барање)",
          link: "https://s-leasing.mk/content/%D0%91%D0%B0%D1%80%D0%B0%D1%9A%D0%B5%20%D0%B7%D0%B0%20%D0%BE%D0%B4%D0%BE%D0%B1%D1%80%D1%83%D0%B2%D0%B0%D1%9A%D0%B5%20%D0%BD%D0%B0%20%D0%BB%D0%B8%D0%B7%D0%B8%D0%BD%D0%B3_Pravni%20Lica-11.01.2022.pdf",
        },
        {
          description: "Копија од тековна состојба, не постара од 6 недели",
        },
        {
          description:
            "Завршна сметка (биланс на состојба и биланс на успех за последните две фискални години)",
        },
        {
          description:
            "Аналитички заклучни листови кон завршните сметки за последните две години",
        },
        {
          description:
            "Аналитички заклучен лист за тековната година со последен датум на книжење",
        },
        {
          description: "Согласност за извадок од Македонско Кредитно Биро",
          linkedText: "(превземи согласност)",
          link: "https://s-leasing.mk/content/%D0%A1%D0%BE%D0%B3%D0%BB%D0%B0%D1%81%D0%BD%D0%BE%D1%81%D1%82%20%D0%B7%D0%B0%20%D0%B8%D0%B7%D0%B2%D0%B0%D0%B4%D0%BE%D0%BA%20%D0%BE%D0%B4%20%D0%9C%D0%B0%D0%BA%D0%B5%D0%B4%D0%BE%D0%BD%D1%81%D0%BA%D0%BE%20%D0%9A%D1%80%D0%B5%D0%B4%D0%B8%D1%82%D0%BD%D0%BE%20%D0%91%D0%B8%D1%80%D0%BE.pdf",
        },
        {
          description: "Изјава за вистински сопственик",
          linkedText: "(превземи согласност)",
          link: "https://s-leasing.mk/content/Izjava-za-vistinski-sopstvenik.pdf",
        },
      ],
    };
  },
};
</script>
