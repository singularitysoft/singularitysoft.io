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
    <div class="container">
      <!-- svelte-ignore a11y-invalid-attribute -->
      <a class="navbar-brand" href="#">Singularity Software</a>
      <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav ml-auto">
          <li class="nav-item">
            <a class="nav-link" href="#about">About</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#features">Features</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#pricing">Pricing</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#contact">Contact</a>
          </li>
        </ul>
      </div>
    </div>
  </nav>
  <section id="hero" class="text-center">
    <div class="container">
      <h1 class="mb-5">Revolutionize your business with AI</h1>
      <p class="lead mb-5">
        Our AI software uses cutting-edge technology to provide you with 
        actionable insights and automate tasks, freeing up time for you to 
        focus on what matters most.
      </p>
    </div>
  </section>
  <section id="about" class="bg-light">
    <div class="container">
      <div class="row">
        <div class="col-lg-8 mx-auto">
          <h2 class="text-center">About Us</h2>
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
  <section id="pricing" class="bg-light">
    <div class="container">
      <h2 class="text-center pricing">Pricing</h2>
      <div class="row">
        <div class="col-lg-4">
          <div class="card">
            <div class="card-body">
              <h4 class="card-title">Basic</h4>
              <p class="card-text">$49/month</p>
              <ul class="list-group">
                <li class="list-group-item">Automated Tasks</li>
                <li class="list-group-item">Limited Insights</li>
                <li class="list-group-item">Basic Support</li>
              </ul>
              <a href="#" class="btn btn-primary">Sign Up</a>
            </div>
          </div>
        </div>
        <div class="col-lg-4">
          <div class="card">
            <div class="card-body">
              <h4 class="card-title">Pro</h4>
              <p class="card-text">$99/month</p>
              <ul class="list-group">
                <li class="list-group-item">Automated Tasks</li>
                <li class="list-group-item">Actionable Insights</li>
                <li class="list-group-item">24/7 Support</li>
              </ul>
              <a href="#" class="btn btn-primary">Sign Up</a>
            </div>
          </div>
        </div>
        <div class="col-lg-4">
         
          <div class="card">
            <div class="card-body">
              <h4 class="card-title">Enterprise</h4>
              <p class="card-text">Custom pricing</p>
              <ul class="list-group">
                <li class="list-group-item">All Features</li>
                <li class="list-group-item">Dedicated Account Manager</li>
                <li class="list-group-item">Customized Solutions</li>
              </ul>
              <a href="#" class="btn btn-primary" on:click={handleClickContact}>Contact Us</a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
  <section id="about">
    <div class="container">
      <h2 class="text-center">About Us</h2>
      <p>We are a team of experts in artificial intelligence and machine learning, committed to providing businesses with innovative solutions that streamline their processes and help them make data-driven decisions. Our AI software is designed to be user-friendly and accessible to businesses of all sizes, so that everyone can reap the benefits of AI technology.</p>
    </div>
  </section>
  <section id="contact">
    <div class="container">
      <h2 class="text-center">Contact Us</h2>
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
    margin-bottom: 36px !important;
  }

  h2 {
    margin-top: 24px;
    margin-bottom: 20px;
  }

  h2.features {
    margin-bottom: 16px;
  }

  h2.pricing {
    margin-top: 0;
    padding-top: 32px;
  }

  p {
    margin-bottom: 8px;
  }

  p.lead {
    margin-bottom: 32px !important;
  }

  ul li {
    /*margin: 16px;*/
  }

  .btn {
    margin-top: 24px;
    margin-bottom: 6px;
  }

  .navbar {
    margin-top: 24px;
    margin-bottom: 32px;
  }

  .container {
    margin-bottom: 24px;
  }

  section#contact .container .form-group {
    text-align: left;
  }

  section#contact .container {
    text-align: center;
  }

  .navbar-expand-lg>.container {
    padding: 8px !important;
    margin-bottom: 8px !important;
  }

  .card {
    text-align: center;
    margin: 16px 0;
  }

  footer {
    padding-top: 26px;
    padding-bottom: 1px;
  }
</style>
