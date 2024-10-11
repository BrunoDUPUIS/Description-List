<script setup>
const firstPerson = {
  gender: 'female',
  firstname: 'Emily',
  lastname: 'Parker',
  age: 24,
  job: 'Teacher',
  hobbies: ['read books', 'go hiking'],
  pet: {
    name: 'Whiskers',
    age: 2,
    species: 'ferret',
  },
}

const secondPerson = {
  gender: 'male',
  firstname: 'Marcus',
  lastname: 'Bennett',
  age: 38,
  job: 'Architect',
  hobbies: ['watch bird', 'play chess'],
  pet: {
    name: 'Nala',
    age: 6,
    species: 'dog',
  },
}

const thirdPerson = {
  gender: 'female',
  firstname: 'Sophia',
  lastname: 'Rodriguez',
  age: 31,
  job: 'Environmental scientist',
  hobbies: ['play guitar', 'bake cakes'],
  pet: {
    name: 'Paws',
    age: 3,
    species: 'cat',
  },
}

const fourthPerson = {
  gender: 'male',
  firstname: 'Oliver',
  lastname: 'Hughes',
  age: 56,
  job: 'Carpenter',
  hobbies: ['paint', 'ride horses'],
  pet: {
    name: 'Bubble',
    age: 4,
    species: 'snake',
  },
}
</script>

<template>
  <main>
    <h1>Description list</h1>
    <div class="cards">
      <div>
        <div>
          <img src="./assets/imgs/emily-parker.jpg" alt="" />
          <h2>{{ firstPerson.firstname }} {{ firstPerson.lastname }}</h2>
          <p>
            {{ firstPerson.gender === 'female' ? 'She' : 'He' }} is a
            {{ firstPerson.age }}-year-old {{ firstPerson.job.toLowerCase() }}.
          </p>
          <p>
            Outside of work, {{ firstPerson.firstname }} likes to
            {{ firstPerson.hobbies[0] }} and {{ firstPerson.hobbies[1] }}.
          </p>
          <p>
            At home,
            {{ firstPerson.gender === 'female' ? 'her' : 'his' }} lively
            companion is {{ firstPerson.pet.name }} a
            {{ firstPerson.pet.age }}-years-old {{ firstPerson.pet.species }}.
          </p>
        </div>
        <font-awesome-icon :icon="['fas', 'heart']" />
      </div>
      <div>
        <div>
          <img src="./assets/imgs/marcus-bennett.jpg" alt="" />
          <h2>{{ secondPerson.firstname }} {{ secondPerson.lastname }}</h2>
          <p>
            {{ secondPerson.gender === 'female' ? 'She' : 'He' }} is a
            {{ secondPerson.age }}-year-old
            {{ secondPerson.job.toLowerCase() }}.
          </p>
          <p>
            Outside of work, {{ secondPerson.firstname }} likes to
            {{ secondPerson.hobbies[0] }} and {{ secondPerson.hobbies[1] }}.
          </p>
          <p>
            At home,
            {{ secondPerson.gender === 'female' ? 'her' : 'his' }} lively
            companion is {{ secondPerson.pet.name }} a
            {{ secondPerson.pet.age }}-years-old {{ secondPerson.pet.species }}.
          </p>
        </div>
        <font-awesome-icon :icon="['fas', 'heart']" />
      </div>
      <div>
        <div>
          <img src="./assets/imgs/sophia-rodriguez.jpg" alt="" />
          <h2>{{ thirdPerson.firstname }} {{ thirdPerson.lastname }}</h2>
          <p>
            {{ thirdPerson.gender === 'female' ? 'She' : 'He' }} is a
            {{ thirdPerson.age }}-year-old {{ thirdPerson.job.toLowerCase() }}.
          </p>
          <p>
            Outside of work, {{ thirdPerson.firstname }} likes to
            {{ thirdPerson.hobbies[0] }} and {{ thirdPerson.hobbies[1] }}.
          </p>
          <p>
            At home,
            {{ thirdPerson.gender === 'female' ? 'her' : 'his' }} lively
            companion is {{ thirdPerson.pet.name }} a
            {{ thirdPerson.pet.age }}-years-old {{ thirdPerson.pet.species }}.
          </p>
        </div>
        <font-awesome-icon :icon="['fas', 'heart']" />
      </div>
      <div>
        <div>
          <img src="./assets/imgs/olivier-hughes.jpg" alt="" />
          <h2>{{ fourthPerson.firstname }} {{ fourthPerson.lastname }}</h2>
          <p>
            {{ fourthPerson.gender === 'female' ? 'She' : 'He' }} is a
            {{ fourthPerson.age }}-year-old
            {{ fourthPerson.job.toLowerCase() }}.
          </p>
          <p>
            Outside of work, {{ fourthPerson.firstname }} likes to
            {{ fourthPerson.hobbies[0] }} and {{ fourthPerson.hobbies[1] }}.
          </p>
          <p>
            At home,
            {{ fourthPerson.gender === 'female' ? 'her' : 'his' }} lively
            companion is {{ fourthPerson.pet.name }} a
            {{ fourthPerson.pet.age }}-years-old {{ fourthPerson.pet.species }}.
          </p>
        </div>
        <font-awesome-icon :icon="['fas', 'heart']" />
      </div>
    </div>
  </main>
</template>

<style scoped>
main {
  padding: 50px;
  min-height: 100vh;
  background-color: #c9e1c2;
}

img {
  width: 100%;
  border-radius: 3px;
  object-position: top;
  aspect-ratio: 16/10;
  margin-bottom: 20px;
}
p {
  line-height: 15px;
  margin-bottom: 5px;
}
.cards {
  /* border: 2px solid blue; */
  gap: 9px;
  display: flex;
}
.cards > div {
  width: calc((100% - 27px) / 4);
  /* border: 1px solid red; */
  padding: 10px;
  background-color: white;
  border-radius: 8px;
  box-shadow: 0 0 9px grey;
  display: flex;
  flex-direction: column;
}
.cards > div > div {
  /* border: 1px solid green; */
}
svg {
  margin-top: 10px;
  color: grey;
  align-self: flex-end;
}

/* ======================= */
/* ==== MEDIA QUERIES ==== */
/* ======================= */

@media (max-width: 1100px) {
  .cards {
    flex-wrap: wrap;
    justify-content: center;
  }
  .cards > div {
    width: 200px;
  }
}

@media (max-width: 500px) {
  .cards > div {
    width: 100%;
  }
}
</style>
