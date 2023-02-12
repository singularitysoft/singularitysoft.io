<script>
  import 'bootstrap/dist/css/bootstrap.min.css';
  import 'jquery/dist/jquery.slim.min.js';
  import 'bootstrap/dist/js/bootstrap.min.js';
  import { onMount } from 'svelte';

  onMount(() => {
    import('popper.js/dist/umd/popper.min.js');
  });

  let clientName = '';
  let clientEmail = '';
  let clientMessage = '';

  function handleClick(evt) {
    evt.preventDefault();
    window.location.href = `mailto:ericgrosse12@gmail.com?cc=${clientEmail}&subject=${`${clientName} - Singularity Software Business Inquiry`}&body=${clientMessage}`;
  }
</script>

<div class="page">
  <nav class="navbar navbar-expand-lg navbar-light bg-light">
    <a class="navbar-brand singularity-brand" href="/">Singularity Software</a> 
  </nav>
  
  <section id="hero" class="text-center">
    <div class="container">
      <h1 class="mb-5">Revolutionize Your Business With SolarisAI</h1>
      <p class="lead solaris-ai-synopsis mb-5">
        Our SolarisAI software uses cutting-edge technology to provide you with 
        actionable insights and automate tasks, freeing up time for you to 
        focus on what matters most.
      </p>
    </div>
  </section>
  <section id="about" class="bg-light">
    <div class="container">
      <div class="row">
        <div class="col-lg-8 mx-auto">
          <h2 class="text-center about-us">About Us</h2>
          <p class="lead">
            We are a team of AI experts and software engineers who are passionate about using technology to solve real-world problems. We believe that AI has the power to transform industries and change the way we work and live for the better. 
          </p>
        </div>
      </div>
    </div>
  </section>
  <section id="features">
    <div class="container">
      <h2 class="text-center features">Features</h2>
      <div class="row">
        <div class="col-lg-4">
          <div class="card">
            <div class="card-body">
              <h4 class="card-title">Automated Tasks</h4>
              <p class="card-text">Our AI software can automate routine and repetitive tasks, freeing up time for you to focus on more important tasks.</p>
            </div>
          </div>
        </div>
        <div class="col-lg-4">
          <div class="card">
            <div class="card-body">
              <h4 class="card-title">Actionable Insights</h4>
              <p class="card-text">Our AI algorithms provide you with actionable insights and predictions, helping you make data-driven decisions.</p>
            </div>
          </div>
        </div>
        <div class="col-lg-4">
          <div class="card">
            <div class="card-body">
              <h4 class="card-title">Intuitive User Interface</h4>
              <p class="card-text">Our software is designed with the user in mind and has an intuitive user interface, making it easy for anyone to use.</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
  <section id="contact">
    <div class="container">
      <h2 class="text-center contact-us">Contact Us</h2>
      <form>
        <div class="form-group">
          <label for="name">Name</label>
          <input type="text" class="form-control" id="name" bind:value={clientName}>
        </div>
        <div class="form-group">
          <label for="email">Email</label>
          <input type="email" class="form-control" id="email" bind:value={clientEmail}>
        </div>
        <div class="form-group">
          <label for="message">Message</label>
          <textarea class="form-control" id="message" rows="3" bind:value={clientMessage}></textarea>
        </div>
        <button on:click={handleClick} class="btn btn-primary">Submit</button>
      </form>
    </div>
  </section>
  <footer class="bg-dark text-white">
    <div class="container">
      <p class="text-center">Copyright &copy; #Singularity #Software (100% Open Source & Free Forever)</p>
    </div>
  </footer>
</div>

<style>
  h1 {
    font-size: 32px;
    margin-top: 48px !important;
    margin-bottom: 36px !important;
  }

  h2.about-us {
    margin-top: 16px;
    margin-bottom: 16px;
  }

  h2.features {
    margin: 24px 0;
  }

  h2.contact-us {
    margin-top: 24px;
    margin-bottom: 16px;
  }
  
  p.lead.solaris-ai-synopsis {
    margin-bottom: 36px !important;
  }

  button {
    margin: 24px 0;
  }

  .navbar {
    background: rgb(33,37,41) !important;
    opacity: 0.9;
    flex-direction: column;
    margin-bottom: 24px;
    padding: 16px;
  }

  a.navbar-brand {
    font-size: 36px;
  }

  a.navbar-brand {
    color: white !important;
  }

  section#contact .container .form-group {
    text-align: left;
  }

  section#contact .container {
    text-align: center;
  }

  .card {
    text-align: center;
  }

  footer {
    padding-top: 26px;
    padding-bottom: 8px;
  }

  .singularity-brand:hover {
    cursor: pointer;
  }
</style>
