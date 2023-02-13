<script>
  import 'bootstrap/dist/css/bootstrap.min.css';

  let clientName = '';
  let clientEmail = '';
  let clientMessage = '';

  function handleClick(evt) {
    evt.preventDefault();
    window.location.href = `mailto:ericgrosse12@gmail.com?cc=${clientEmail}&subject=${`${clientName} - Singularity Software Business Inquiry`}&body=${clientMessage}`;
  }
</script>

<div class="page">
  <nav>
    <span>Singularity Software</span> 
  </nav>
  
  <section id="hero" class="text-center">
    <div class="container">
      <h1 class="mb-5">Revolutionize Your Business With SolarisAI</h1>
      <p class="lead mb-5">
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
  <footer>
    <a href="https://linkedin.com/in/eric-grosse">
      <svg class="linkedin-icon" viewBox="0 0 24 24">
        <path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433c-1.144 0-2.063-.926-2.063-2.065 0-1.138.92-2.063 2.063-2.063 1.14 0 2.064.925 2.064 2.063 0 1.139-.925 2.065-2.064 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24H22.225c.979 0 1.771-.773 1.771-1.729v-20.542C23.996.774 23.204 0 22.225 0z"/>
      </svg>
    </a>
    <a href="https://github.com/singularitysoft">
      <svg class="github-icon" viewBox="0 0 24 24">
        <path d="M12 .297c-6.63 0-12 5.373-12 12 0 5.303 3.438 9.8 8.205 11.385.6.113.82-.258.82-.577 0-.285-.01-1.04-.015-2.04-3.338.724-4.042-1.61-4.042-1.61C4.422 18.07 3.633 17.7 3.633 17.7c-1.087-.744.084-.729.084-.729 1.205.084 1.838 1.236 1.838 1.236 1.07 1.835 2.809 1.305 3.495.998.108-.776.417-1.305.76-1.605-2.665-.3-5.466-1.332-5.466-5.93 0-1.31.465-2.38 1.235-3.22-.135-.303-.54-1.523.105-3.176 0 0 1.005-.322 3.3 1.23.96-.267 1.98-.399 3-.405 1.02.006 2.04.138 3 .405 2.28-1.552 3.285-1.23 3.285-1.23.645 1.653.24 2.873.12 3.176.765.84 1.23 1.91 1.23 3.22 0 4.61-2.805 5.625-5.475 5.92.42.36.81 1.096.81 2.22 0 1.606-.015 2.896-.015 3.286 0 .315.21.69.825.57C20.565 22.092 24 17.592 24 12.297c0-6.627-5.373-12-12-12"/>
      </svg>
    </a>
    <a href="mailto:ericgrosse12@gmail.com">
      <svg class="mail-icon" viewBox="0 0 24 24">
        <path d="M20 4H4c-1.1 0-1.99.9-1.99 2L2 18c0 1.1.9 2 2 2h16c1.1 0 2-.9 2-2V6c0-1.1-.9-2-2-2zm0 4l-8 5-8-5V6l8 5 8-5v2z"/>
      </svg>
    </a>
  </footer>
</div>

<style>
  h1 {
    font-size: 32px;
    margin-top: 36px !important;
    margin-bottom: 28px !important;
  }

  h2.about-us {
    margin-top: 28px;
    margin-bottom: 16px;
  }

  h2.features {
    margin: 24px 0;
  }

  h2.contact-us {
    margin-top: 24px;
    margin-bottom: 16px;
  }

  h4 {
    margin-bottom: 24px;
  }
  
  p.lead {
    margin-bottom: 36px !important;
  }

  button {
    margin: 24px 0;
  }

  nav {
    margin-top: -8px;
    padding: 16px;
    background: rgb(33,37,41);
    opacity: 0.9;
    text-align: center;
  }

  nav span {
    font-size: 36px;
    color: white;
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

  .card-body {
    padding: 32px;
  }

  footer {
    border-top: 1px solid #0000002b;
    padding-top: 26px;
    padding-bottom: 8px;
    text-align: center;
  }

  footer a {
    padding: 0 5px;
  }

  svg {
    fill: rgb(33,37,41);
    transition: fill 0.25s;
  }

  svg:hover {
    fill: rgb(102,102,102);
    width: 50px;
    height: 50px;
  }

  svg.github-icon {
    width: 50px;
    height: 50px;
  }

  svg.linkedin-icon {
    width: 50px;
    height: 50px;
  }

  svg.mail-icon {
    width: 50px;
    height: 50px;
  }
</style>
