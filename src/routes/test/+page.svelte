<script lang="ts">
  import { scale } from "svelte/transition";

  let background_container: HTMLDivElement;
  let scrolling_container: HTMLDivElement;

  let innerHeight: number;
  let innerWidth: number;

  const section_map = {
    title: "/img4.jpg",
    timeline: "/img4.jpg",
    about: "/img4.jpg",
    section1: "/img1.jpg",
    section2: "/img2.jpg",
    section3: "/img3.jpg",
  };
  let current_section = "title";
  const scroll_handler = (e: UIEvent) => {
    let current_section_id = find_inview_section();
    if (current_section_id)
      if (current_section_id !== current_section) {
        change_background(
          section_map[current_section_id as keyof typeof section_map]
        );
        current_section = current_section_id;
      }
  };

  const find_inview_section = () => {
    let elements = document.elementsFromPoint(innerWidth / 2, innerHeight / 2);
    let section = elements.find((el) => el.id);

    return section?.id;
  };

  const change_background = (img: string) => {
    if (
      background_container.style.getPropertyValue("background-image") ===
      `url(${img})`
    )
      return;
    background_container?.style.setProperty("background-image", `url(${img})`);
  };
</script>

<svelte:window bind:innerHeight bind:innerWidth on:scroll={scroll_handler} />

<main class="relative">
  <div class="sticky top-0 left-0 overflow-clip -z-50">
    <div
      class="background-container bg-cover w-screen h-screen bg-center"
      style="background-image: url(/img4.jpg);"
      bind:this={background_container}
    ></div>
    <!-- background -->
  </div>

  <div
    class="z-50 flex flex-col justify-start -translate-y-[50vh]"
    bind:this={scrolling_container}
  >
    <!-- scrolling content -->

    <div
      id="title"
      class="h-screen flex justify-center items-center -translate-y-[50vh]"
    >
      <h1
        class="text-4xl text-white font-bold w-full h-full flex items-center justify-center"
      >
        Discriminatory Laws affecting South Asians across Canada
      </h1>
    </div>

    <div id="about" class="section">
      <h2>About</h2>
      <p>
        Canada, known for its multicultural society and commitment to human
        rights, has a history marked by discriminatory laws, policies, and
        practices targeted at various communities. This platform aims to shed
        light on the development of racist laws and practices against South
        Asians in Canada. Exploring the historical records, we seek to
        illuminate the adversities, obstacles, and victories of the South Asian
        community in dealing with systemic prejudice.
      </p>
    </div>
    <div id="section1" class="section">
      <h2>Immigration Act 1906 and continuous journey Act 1908</h2>
      <p>
        The Immigration Act of 1906 marked a significant shift towards stricter
        immigration policies. It broadened the list of forbidden immigrant
        categories, established a formalized deportation procedure, and granted
        the government expanded authority to exercise discretionary judgments
        regarding admission.<br /><br />
        An amendment to the Immigration Act was made in 1908 to incorporate the "continuous
        journey regulation" of the Canadian government, which forbade the entry into
        Canada of any immigrant who had not traveled continuously from the place
        of their birth or citizenship. As most voyages from the region involved stops,
        this posed a considerable obstacle to immigrants from South Asia.
      </p>
    </div>
    <div id="section2" class="section">
      <h2>Dominion Elections Act</h2>
      <p>
        In 1920, the Dominion Elections Act resulted in the removal of federal
        voting privileges for those who had been denied the right to vote at the
        provincial level due to their ethnicity, particularly impacting people
        of Chinese, Japanese, and South Asian descent in British Columbia.
        Moreover, individuals of Chinese origin in Saskatchewan were also denied
        their right to vote.
      </p>
    </div>
    <div id="section3" class="section">
      <h2>The Komagata Maru Incident</h2>
      <p>
        This incident unfolded during the spring and summer of 1914, just before
        the onset of the First World War. It turned out to be a harrowing and
        sorrowful ordeal for the passengers involved. Initially, there was an
        unsuccessful attempt at confrontation with officials, police, and the
        military at the Port of Vancouver. Subsequently, as the passengers
        returned to India, they faced a tragic and fatal clash with police and
        troops near Kolkata. The Komagata Maru tale illustrates the Canadian
        government's purposeful exclusionary policy toward ethnic groups it
        deemed unfit to enter. These defenses of Canada's continued status as a
        "White Man's Country" were couched in racist and ethnocentric notions of
        "progress," "civilization," and "suitability."
      </p>
    </div>
  </div>
</main>

<div class="flex flex-col items-center justify-center py-20">

  <h2 class="text-4xl font-semibold border-b-2 pb-6 w-[80%] text-center">A Timeline of Events</h2>

  <div id="timeline" class="flex items-center justify-center h-screen w-full">
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

<style type="postcss">
  .section {
    @apply m-56 p-14 flex flex-col items-center justify-center gap-10 text-black text-center;
    background: url("/text-bg.jpg");
    background-size: cover;
    clip-path: polygon(
      3% 0,
      7% 1%,
      11% 0%,
      16% 2%,
      20% 0,
      23% 2%,
      28% 2%,
      32% 1%,
      35% 1%,
      39% 3%,
      41% 1%,
      45% 0%,
      47% 2%,
      50% 2%,
      53% 0,
      58% 2%,
      60% 2%,
      63% 1%,
      65% 0%,
      67% 2%,
      69% 2%,
      73% 1%,
      76% 1%,
      79% 0,
      82% 1%,
      85% 0,
      87% 1%,
      89% 0,
      92% 1%,
      96% 0,
      98% 3%,
      99% 3%,
      99% 6%,
      100% 11%,
      98% 15%,
      100% 21%,
      99% 28%,
      100% 32%,
      99% 35%,
      99% 40%,
      100% 43%,
      99% 48%,
      100% 53%,
      100% 57%,
      99% 60%,
      100% 64%,
      100% 68%,
      99% 72%,
      100% 75%,
      100% 79%,
      99% 83%,
      100% 86%,
      100% 90%,
      99% 94%,
      99% 98%,
      95% 99%,
      92% 99%,
      89% 100%,
      86% 99%,
      83% 100%,
      77% 99%,
      72% 100%,
      66% 98%,
      62% 100%,
      59% 99%,
      54% 99%,
      49% 100%,
      46% 98%,
      43% 100%,
      40% 98%,
      38% 100%,
      35% 99%,
      31% 100%,
      28% 99%,
      25% 99%,
      22% 100%,
      19% 99%,
      16% 100%,
      13% 99%,
      10% 99%,
      7% 100%,
      4% 99%,
      2% 97%,
      1% 97%,
      0% 94%,
      1% 89%,
      0% 84%,
      1% 81%,
      0 76%,
      0 71%,
      1% 66%,
      0% 64%,
      0% 61%,
      0% 59%,
      1% 54%,
      0% 49%,
      1% 45%,
      0% 40%,
      1% 37%,
      0% 34%,
      1% 29%,
      0% 23%,
      2% 20%,
      1% 17%,
      1% 13%,
      0 10%,
      1% 6%,
      1% 3%
    );
  }
  .section h2 {
    @apply text-4xl font-semibold;
  }
  .section p {
    @apply text-xl;
  }

  .background-container {
    user-select: none;
    -webkit-user-select: none;
    -moz-user-select: none;
    -ms-user-select: none;
    -webkit-animation: zoomin 40s ease-in;
    animation: zoomin 40s ease-in;
    transition: all 0.4s linear;
    overflow: hidden;
  }

  /* Zoom in Keyframes */
  @-webkit-keyframes zoomin {
    0% {
      transform: scale(1);
    }
    50% {
      transform: scale(1.5);
    }
    100% {
      transform: scale(1);
    }
  }
  @keyframes zoomin {
    0% {
      transform: scale(1);
    }
    50% {
      transform: scale(1.5);
    }
    100% {
      transform: scale(1);
    }
  } /*End of Zoom in Keyframes */
</style>
