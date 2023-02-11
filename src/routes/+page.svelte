<script>
  import 'bootstrap/dist/css/bootstrap.min.css';
  import 'jquery/dist/jquery.slim.min.js';
  import 'popper.js/dist/umd/popper.min.js';
  import 'bootstrap/dist/js/bootstrap.min.js';

  function handleClickContact(evt) {
    evt.preventDefault();
    console.log('handleClickContact');
    window.location.href = 'mailto:myaddress@email.com?subject= Software Singularity Business Inquiry';;
  }

  function handleSubmit(event) {
    event.preventDefault();
    const name = document.getElementById("name").value;
    const email = document.getElementById("email").value;
    const message = document.getElementById("message").value;
    const subject = `Contact from ${name}`;
    const body = `Email: ${email}\nMessage: ${message}`;
    window.location.href = `mailto:ericgrosse1@gmail.com?subject=${subject}&body=${body}`;
  }
</script>

<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta http-equiv="X-UA-Compatible" content="ie=edge">
  <title>Singularity Software</title>
</head>
<body>
  
  

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
          <input type="text" class="form-control" id="name">
        </div>
        <div class="form-group">
          <label for="email">Email</label>
          <input type="email" class="form-control" id="email">
        </div>
        <div class="form-group">
          <label for="message">Message</label>
          <textarea class="form-control" id="message" rows="3"></textarea>
        </div>
        <button on:click={handleSubmit} type="submit" class="btn btn-primary">Submit</button>
      </form>
    </div>
  </section>
  <footer class="bg-dark text-white">
    <div class="container">
      <p class="text-center">Copyright &copy; #Singularity #Software (100% Open Source & Free Forever)</p>
    </div>
  </footer>
</body>
</html>

<style>
  h1 {
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

  a.navbar-brand, a.nav-link {
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
