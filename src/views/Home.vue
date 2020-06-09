<template>
  <div class="row">
    <div class="col-12 col-md-12">
      <b-card tag="article" class="hero">
        <img class="logo" alt="OpenUBI Project logo" src="../assets/open-ubi-project-logo-no-padding.svg">
        <h1>Sharing best practices for <em>implementing</em> Universal Basic Income around the world.</h1>
      </b-card>
    </div>
    <div class="col-12 col-md-4">
      <a href="https://github.com/OpenUBIProject/OpenUBI/raw/master/Policy-Brief-UBI-Impl.pdf" target="_blank">
        <b-card
                title="Implementing Nationwide Universal Basic Income"
                tag="article"
                footer="View Policy Brief (PDF)"
        >
          <b-card-text>
            <div>
              This policy brief is a well-cited document that addresses:
              <ul>
                <li>advancements with work in the 21st century</li>
                <li>why we need economic security</li>
                <li>how technology enables UBI</li>
                <li>best practices for creating UBI policies</li>
              </ul>
            </div>
          </b-card-text>
        </b-card>
      </a>
    </div>
    <div class="col-12 col-md-4">
      <a href="#">
        <b-card
                title="Action Framework"
                tag="article"
                footer="Learn More"
        >
          <b-card-text>
            <!-- TODO -->
            This sample description describes the OpenUBI Action Framework that can be used to develop specific policy for implementing UBI.
          </b-card-text>
        </b-card>
      </a>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.hero .card-body {
  display: flex;
  flex-direction: column;
  text-align: left;
  padding: 40px;

  .logo {
    max-height: 120px;
    width: 100%;
    margin: 0 0 30px;
  }

  h1 {
    text-align: left;
    font-weight: 300;
    margin: 0;
    font-size: 2rem;
    line-height: 1.3;
  }
}

@media (min-width: 380px) {
  .hero .card-body {
    .logo {
      max-height: 150px;
    }

    h1 {
      font-size: 2.5rem;
    }
  }
}

@media (min-width: 992px) {
  .hero .card-body {
    flex-direction: row-reverse;
    align-items: center;
    text-align: center;
    padding: 40px 60px;

    .logo {
      max-height: 160px;
      width: auto;
      margin: 0;
    }

    h1 {
      font-size: 2.7rem;
      line-height: 1.4;
    }
  }
}

@media (min-width: 1200px) {
  .hero .card-body {
    padding: 50px 90px;

    .logo {
      max-height: 175px;
    }

    h1 {
      font-size: 3rem;
    }
  }
}
</style>