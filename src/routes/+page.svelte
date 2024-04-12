<script lang="ts">
  import { Parallax, ParallaxLayer } from "svelte-parallax";
</script>

<Parallax sections={3}>
  <ParallaxLayer offset={0} rate={-0.1}>
    <div
      class="background-container bg-cover w-screen h-screen bg-center transition-all duration-500 ease-in-out"
      style="background-image: url(./img4.jpg);"
    ></div>
  </ParallaxLayer>

  <ParallaxLayer offset={0} rate={1.3}>
    <div id="title" class="h-screen flex justify-center items-center">
      <h1
        class="text-6xl text-[#ffffff] font-bold flex h-full w-full items-center justify-center text-center bg-[#5353537f]"
      >
        Timeline of Discriminatory Laws: A South Asian History
      </h1>
    </div>
  </ParallaxLayer>

  <ParallaxLayer offset={1} rate={0.1}>

    <div
      id="about"
      class="flex flex-row items-center justify-center h-screen w-full p-20 bg-[#f3f3f3] gap-10"
    >
      <div class="flex flex-col gap-10 w-1/2">
        <h2 class="font-bold text-6xl">About</h2>
        <p class="text-lg">
          Canada, known for its multicultural society and commitment to human
          rights, has a history marked by discriminatory laws, policies, and
          practices targeted at various communities. This platform aims to shed
          light on the development of racist laws and practices against South
          Asians in Canada. Exploring the historical records, we seek to
          illuminate the adversities, obstacles, and victories of the South
          Asian community in dealing with systemic prejudice.
        </p>
      </div>
      
      <div class="w-1/2">
        <img src="./img2.jpg" alt="img" class="rounded-lg" />
      </div>
    </div>

    <div class="flex flex-col items-center h-screen justify-center pt-20">
      <h2 class="text-4xl font-semibold border-b-2 pb-6 w-[80%] text-center">
        A Timeline of Discriminatory laws
      </h2>

      <div
        id="timeline"
        class="flex items-center justify-center h-screen w-full"
      >
        <iframe
          src="https://cdn.knightlab.com/libs/timeline3/latest/embed/index.html?source=132DfhxF5iJTrjHiVMfGkVyMojIg2gbqaViMSO1Uu_kY&font=Default&lang=en&initial_zoom=2&height=650"
          width="85%"
          height="650"
          allowfullscreen
          frameborder="0"
          title="Timeline"
        ></iframe>
      </div>
    </div>
  </ParallaxLayer>
</Parallax>
