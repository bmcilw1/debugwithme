<!-- Home -->
<section id="home" class="section hero is-primary is-medium">
  <div class="hero-body">
    <h1 class="title">DebugWithMe</h1>

    <h2 class="subtitle">Let's tackle this one together</h2>
  </div>
</section>

<!-- Problem -->
<section id="problem" class="section">
  <div class="container is-max-desktop">
    <h1 class="title my-6 has-text-centered">Debugging can be</h1>
    <div class="tile is-ancestor">
      <div class="tile is-vertical is-8">
        <div class="tile">
          <div class="tile is-parent is-vertical">
            <article class="tile is-child notification is-warning">
              <p class="title">Time consuming</p>
            </article>
            <article class="tile is-child notification is-danger">
              <p class="title">...stressful!</p>
            </article>
          </div>
          <div class="tile is-parent is-2">
            <article
              class="tile is-child notification is-info has-text-vertical is-centered"
            >
              <div class="title">Unpredictable</div>
            </article>
          </div>
        </div>
      </div>
      <div class="tile is-parent is-4">
        <article class="tile is-child notification is-success">
          <div class="content">
            <p class="title">Just plain</p>
            <p class="subtitle">HARD</p>
          </div>
        </article>
      </div>
    </div>
    <div class="title is-parent">
      <div class="tile is-child notification is-link">
        And we spend SO much of our time doing it! 😭
      </div>
    </div>
  </div>
</section>

<!-- Existing Solutions -->
<section id="existing-solutions" class="section is-medium">
  <div class="container">
    <article class="message is-info">
      <div class="message-body">We can find answers to specifics online.</div>
    </article>
    <article class="message is-success">
      <div class="message-body">But, what if we don't know where to start?</div>
    </article>
    <article class="message is-warning">
      <div class="message-body">
        There seems to be a lack of <span class="has-text-primary">general</span
        > debugging resources.
      </div>
    </article>
  </div>
</section>

<!-- Solution -->
<section id="solution" class="section is-large">
  <div class="container">
    <div class="columns">
      <div class="column is-8 content">
        <ol>
          <li>I'm creating videos debugging real problems for free!</li>
          <li>You send in a request, and I'll do my best to help.</li>
          <li>
            We'll record the experience and post it online to help others.
          </li>
          <li>When I can't help, the community probably can!</li>
        </ol>
      </div>
    </div>
  </div>
</section>

<!-- Contact -->
<section id="contact" class="section is-large">
  <div class="columns is-centered">
    <div class="column is-8">
      <form name="contact-form" data-netlify="true" method="POST">
        <div class="field">
          <label class="label" for="guest-name">Name</label>
          <div class="control">
            <input
              class="input"
              name="guest-name"
              type="text"
              placeholder="Your name"
            />
          </div>
        </div>
        <div class="field">
          <label class="label" for="email">Email</label>
          <div class="control">
            <input
              class="input"
              name="email"
              type="email"
              placeholder="Your email"
            />
          </div>
        </div>
        <div class="field">
          <label class="label" for="description">Bug Descripton</label>
          <div class="control">
            <textarea
              class="textarea"
              name="description"
              placeholder="Describe the bug you're working on..."
            />
          </div>
        </div>
        <div class="field">
          <div class="control">
            <button type="submit" class="button is-primary">Submit</button>
          </div>
        </div>
      </form>
    </div>
  </div>
</section>

<!-- Footer -->
<footer class="footer">
  <div class="content has-text-centered">
    Copyright © 2021
    <a href="https://technicallyemployed.com">Technically Employed</a>
  </div>
</footer>
