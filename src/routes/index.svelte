<script>
  import ImageCard from "@components/ImageCard.svelte";

  let property = {
    imageUrl: "PALETAS.jpg",
    imageAlt: "Paletas",
    beds: 3,
    baths: 2,
    title: "Paletas heladas",
    priceInCents: 190000,
    formattedPrice: "$1,900.00",
    reviewCount: 34,
    rating: 4
  };
</script>

<svelte:head>
  <title>Sapper project template</title>
</svelte:head>

<ImageCard {property} />
