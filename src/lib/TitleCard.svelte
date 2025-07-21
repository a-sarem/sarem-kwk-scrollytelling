<script>
  let { title, subtitle } = $props();
</script>

<div class="title-card">
  <div class="content">
    <h1>{title}</h1>
    <p>{subtitle}</p>
  </div>
</div>

<style>
  .title-card {
    background-color: rgb(95, 76, 143);
    background-size: cover;
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
    padding: 2rem;
    box-sizing: border-box;
    font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
  }

  .content {
    max-width: 700px;
    background-image: url("gradiant.jpg");
    background-size: cover;
    padding: 2rem;
    border: 2px solid black;
    border-radius: 2rem;
    box-shadow: 16px 16px #260f62;
  }

  h1 {
    font-size: 30px;
    font-family: "Courier New", monospace;
    margin: 1rem;
    color: white;
    text-shadow: 1px 1px 0 black;
  }

  p {
    font-size: 1.3rem;
    font-family: "Courier New", monospace;
    color: white;
    margin-top: 1rem;
    text-shadow: 1px 1px 0 black;
  }

  @media (max-width: 600px) {
    h1 {
      font-size: 2.2rem;
    }

    p {
      font-size: 1.1rem;
    }
  }
</style>
