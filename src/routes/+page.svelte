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
    <div id="title" class="h-screen flex justify-center items-end bg-[#5353537f]">
      <h1
        class="lg:text-4xl md:text-6xl text-3xl text-[#ffffff] px-[15%] lg:pb-16 md:pb-16 pt-36 font-semibold flex flex-col gap-4 w-full items-center text-center font-mono"
      >
        Timeline of Discriminatory Laws: A South Asian History
        <span class="lg:text-base md:text-base text-sm font-normal px-[10%]">
Exploring the historical records, we seek to
          illuminate the adversities, obstacles, and victories of the South
          Asian community in dealing with systemic prejudice.
        </span>
      </h1>
    </div>
  </ParallaxLayer>

  <ParallaxLayer offset={1} rate={0.1}>

    <div
      id="about"
      class="flex lg:flex-row md:flex-row flex-col items-center justify-center h-screen w-full lg:pl-20 md:pl-20 lg:p-0 md:p-0 p-10 gap-10 bg-[#f3f3f3]"
    >
      <div class="flex flex-col gap-10 font-mono">
        <h2 class="font-bold lg:text-6xl md:text-6xl text-4xl">About</h2>
        <p class="lg:text-lg md:text-lg text-sm">
          Canada, known for its multicultural society and commitment to human
          rights, has a history marked by discriminatory laws, policies, and
          practices targeted at various communities. This platform aims to shed
          light on the development of racist laws and practices against South
          Asians in Canada. 
        </p>
      </div>

      <div class="min-w-[50vw] h-full">
        <img src="./img2.jpg" alt="img" class="w-full h-full object-cover" />
      </div>
    </div>

    <div class="flex flex-col items-center h-screen justify-center pt-20">
      <h2 class="text-4xl font-semibold border-b-2 pb-6 w-[80%] text-center font-mono">
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
          class="border shadow-lg"
        ></iframe>
      </div>
    </div>
  </ParallaxLayer>
</Parallax>
