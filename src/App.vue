<!-- single file components: SFC. -->

<!-- Lógica JavaScript y reactividad -->
<script setup>
// Para el ejemplo de añadiendo picture de otra manera: import catPicture from './assets/images/gato.png' -->
import IdCard from './components/IdCard.vue';
import Random from './components/Random.vue';
import BoxColor from './components/BoxColor.vue';
import CreditCard from './components/CreditCard.vue';
import Rating from './components/Rating.vue';
import DriverCard from './components/DriverCard.vue';
import LikeButton from './components/LikeButton.vue';
import Carousel from './components/Carousel.vue';
import FaceBook from './components/FaceBook.vue';

</script>

<!-- HTML y directivas Vue -->
<template>
  <div>
    <h1>Creación de componentes con Vue</h1>
    <p>Crea a continuación todos los componentes del ejercicio.</p>
    <h2>1-Id Card</h2>
    <IdCard first-name='John' last-name='Doe' gender='male' :height="178" :birth="new Date('1992-07-14')"
      picture="https://randomuser.me/api/portraits/men/44.jpg" />
      <!-- Es interesante pasar un objeto de tipo fecha en vez de un string tipo '1988-05-11' porque de este tipo de objeto puedes extraer un formato de fecha, puedes comparar fechas, etc -->
    <IdCard last-name='Delores' first-name='Obrien' gender='female' :height="172" :birth="new Date('1993-05-11')"
      picture="https://randomuser.me/api/portraits/women/44.jpg" />

    <h2>Random</h2>
    <Random :min="1" :max="6"></Random>
    <Random :min="1" :max="100"></Random>

    <h2>RGB Color</h2>
    <BoxColor :r="255" :g="0" :b="0" />
    <BoxColor :r="128" :g="255" :b="0" />

    <h2>Credit Card</h2>
    <CreditCard type="visa" bg-color="#11aa99" number="0123456789018845" :expiration-month="3" :expiration-year="2021"
    bank="BNP" owner="Maxence Bourete" />
    <CreditCard type="mastercard" bg-color="#000000" number="0123456789010995" :expiration-month="3" :expiration-year="2021"
    bank="N26" owner="Maxence Bourete" />
    <CreditCard type="visa" bg-color="#ffd700" number="0123456789016984" :expiration-month="12" :expiration-year="2019"
    bank="Name of the Bank" owner="FirstName LastName" />

    <h2>Rating</h2>
    <Rating :rate="0" />
    <Rating :rate="1.49" />
    <Rating :rate="1.5" />
    <Rating :rate="3" />
    <Rating :rate="4" />
    <Rating :rate="5" />

    <h2>DriverCard</h2>
    <DriverCard name='Travis Kalanick' :rating="4.2" img="https://si.wsj.net/public/resources/images/BN-TY647_37gql_OR_20170621052140.jpg?width=620&height=428" :car="{ model: 'Toyota Corolla Altis', licensePlate: 'CO42DE' }" />
    <DriverCard name='Dara Khosrowshahi' :rating="4.9" img="https://ubernewsroomapi.10upcdn.com/wp-content/uploads/2017/09/Dara_ELT_Newsroom_1000px.jpg" :car="{ model: 'Audi A3', licensePlate: 'BE33ER' }" />

    <h2>Like Button</h2>
    <LikeButton />

    <h2>Carousel</h2>
    <Carousel :images="[
      'https://randomuser.me/api/portraits/women/1.jpg',
      'https://randomuser.me/api/portraits/men/1.jpg',
      'https://randomuser.me/api/portraits/women/2.jpg',
      'https://randomuser.me/api/portraits/men/2.jpg'
    ]"

    <h2>FaceBook</h2>
    <FaceBook />
    

/>
  </div>
</template>
<!-- Ejemplo añadiendo picture de otra manera: <IdCard last-name='Garcia' first-name='Loki' gender='male' :height="172" :birth="new Date('1988-05-11')" :picture="catPicture" /> -->

<!-- Estilos. Con el modificador "scoped" permite que estos estilos solo se apliquen a este componente -->
<style scoped>
h2 {
  margin: 1rem 0;
}
</style>

