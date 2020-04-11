<script>
  import ImageCard from "@components/ImageCard.svelte";

  let course = {
    imageUrl: "man.jpg",
    imageAlt: "Vision Artificial",
    weeks: 3,
    modules: 2,
    title: "Vision Artificial en tiempos de redes convolucionales profundas",
    priceInCents: 190000,
    formattedPrice: "$1,900.00",
    reviewCount: 34,
    rating: 4
  };
</script>

<svelte:head>
  <title>Sapper project template</title>
</svelte:head>

<ImageCard {course} />
