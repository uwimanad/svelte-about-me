<script>
  let name = "Divine Uwimana"; // Change this to your name
  let favoriteNumber = 7; // Change this to your favorite number
  let bio = "I am a web developer with a passion for DATA science";
  let hobbies = ["Coding", "Badminton", "Baking"]; // List some hobbies
  import ImageCard from "./lib/ImageCard.svelte";

  let cardData = [
    {
      image:
        "https://images.stockcake.com/public/b/6/f/b6fc5bc0-d7fe-4e38-830e-4a06b60bd1a9_large/coding-coffee-break-stockcake.jpg",
      title: "Coding",
      description:
        "I love solving problems and writing code to build cool things.",
    },
    {
      image:
        "https://mekreview.com/wp-content/uploads/2021/03/clay-banks-w_qTfiPbjbg-unsplash-scaled.jpg",
      title: "Reading",
      description: "Books help me grow intellectually and creatively.",
    },
    {
      image:
        "https://images.unsplash.com/photo-1597528662465-55ece5734101?fm=jpg&q=60&w=3000&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxzZWFyY2h8M3x8YmFraW5nfGVufDB8fDB8fHww",
      title: "Baking",
      description: "I enjoy making cakes and cookiess",
    },
  ];
</script>

<div class="container">
  <h1>About Me</h1>
  <p>Hello, my name is <strong>{name}</strong>!</p>
  <p>My favorite number is <strong>{favoriteNumber}</strong>.</p>
  <p>{bio}</p>

  <h2>My Hobbies</h2>
  <h2>Some of My Favorite Things</h2>
  <div class="card-container">
    {#each cardData as { image, title, description }}
      <ImageCard {image} {title} {description} />
    {/each}
  </div>
  <div class="hobbies">
    {#each hobbies as hobby}
      <div class="hobby">{hobby}</div>
    {/each}
  </div>
</div>

<style>
  h1 {
    color: #f3f4f5;
    font-family: Arial, sans-serif;
  }
  .container {
    max-width: 800px;
    margin: 0 auto;
    padding: 20px;
    text-align: center;
  }
  .hobbies {
    display: flex;
    justify-content: center;
    gap: 15px;
    flex-wrap: wrap;
  }
  .hobby {
    background-color: #1b4b43;
    color: white;
    padding: 10px 15px;
    border-radius: 5px;
  }
</style>
