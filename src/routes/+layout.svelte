<script>
  import "../app.css";

  import Header from "$lib/Header.svelte";
  import Footer from "$lib/Footer.svelte";
</script>

<svelte:head>
  <title>South Asian Discriminatory Laws</title>

  <link
    href="https://fonts.googleapis.com/css?family=Lato:300,400,700,300italic,400italic,700italic"
    rel="stylesheet"
    type="text/css"
  />
  <!-- <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css"> -->
  <script src="https://kit.fontawesome.com/30f055fc02.js" crossorigin="anonymous"></script>

</svelte:head>

<Header />

<slot />

<Footer />