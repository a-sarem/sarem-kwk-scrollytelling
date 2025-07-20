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
    background-image: url("gradiant.jpg");
    background-size: cover;
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
    padding: 2rem;
    box-sizing: border-box;
    font-family: "Inter", sans-serif;
  }

  .content {
    max-width: 700px;
    background-color: #5d5bb9;
    padding: 2rem;
    border: 6px solid #0a0685;
    border-radius: 2rem;
    box-shadow: 16px 16px #260f62;
  }

  h1 {
    font-size: 40px;
    font-family:'Narrow';
    margin: 0;
    color: white;
    text-shadow: 1px 1px 0 #007052;
  }

  p {
    font-size: 1.3rem;
    font-family: Narrow;
    color: white;
    margin-top: 1rem;
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
