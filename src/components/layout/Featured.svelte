<script>
	let current = '';
</script>
<div class="cards">
  <div class="cardContainer inactive">
    <button class="cardd" class:active={current == 'first'} on:click={() => current = current == 'first' ? '' : 'first'}>
      <div class="side front">
        <div class="img img1"></div>
        <div class="info">
          <h2>Super S</h2>
          <p>A stand-on with an exceptional compact stance. Great for tight spaces and trailering.</p>
        </div>
      </div>
      <div class="side back">
        <div class="info">
          <h2>At a glance</h2>
          <ul>
            <li>Manage backyard gates with ease with the 36" deck option</li>
            <li>Your choice of deck sizes ranging from 36", 48", 52" and 60"</li>
            <li>Updated hip bolstering offers superior operator comfort and positioning</li>
          </ul>
          <a class="btn" href="#contact">
            <h4>Learn More</h4>
            <svg fill="#333" height="24" viewBox="0 0 24 24" width="24" xmlns="http://www.w3.org/2000/svg"><path d="M8.59 16.34l4.58-4.59-4.58-4.59L10 5.75l6 6-6 6z"/><path d="M0-.25h24v24H0z" fill="none"/></svg>
          </a>
        </div>
      </div>
    </button>
  </div>

  <div class="cardContainer inactive">
    <button class="cardd" class:active={current == 'second'} on:click={() => current = current == 'second' ? '' : 'second'}>
      <div class="side front">
        <div class="img img2"></div>
        <div class="info">
          <h2>Super Z HyperDrive</h2>
          <p>A high-performance zero-turn with unsurpassed strength, speed &amp; reliability with a warranty to match.</p>
        </div>
      </div>
      <div class="side back">
        <div class="info">
          <h2>At a glance</h2>
          <ul>
            <li>Your choice of VX4 decks ranging from 60 to 72 inches</li>
            <li>The 37hp Vanguard BigBlock EFI makes short work out of big jobs enabling speeds up to 16mph</li>
            <li>Massive 24" drive tires and 13" front caster tires</li>
          </ul>
          <a class="btn" href="#contact">
            <h4>Learn More</h4>
            <svg fill="#333" height="24" viewBox="0 0 24 24" width="24" xmlns="http://www.w3.org/2000/svg"><path d="M8.59 16.34l4.58-4.59-4.58-4.59L10 5.75l6 6-6 6z"/><path d="M0-.25h24v24H0z" fill="none"/></svg>
          </a>
        </div>
      </div>
    </button>
  </div>

  <div class="cardContainer inactive">
    <button class="cardd" class:active={current == 'third'} on:click={() => current = current == 'third' ? '' : 'third'}>
      <div class="side front">
        <div class="img img3"></div>
        <div class="info">
          <h2>Vanguard Power</h2>
          <p>If you need a tough, commercial grade engine that makes you more productive, look to Vanguard.</p>
        </div>
      </div>
      <div class="side back">
        <div class="info">
          <h2>At a glance</h2>
          <ul>
            <li>V-Twin OHV Technology provides superior balance, low vibration, lower emissions, better fuel economy and higher HP/Weight</li>
            <li>Advanced Debris Management keeps engine clean and cool for enhanced durability and performance</li>
          </ul>
          <a class="btn" href="#contact">
            <h4>Learn More</h4>
            <svg fill="#333" height="24" viewBox="0 0 24 24" width="24" xmlns="http://www.w3.org/2000/svg"><path d="M8.59 16.34l4.58-4.59-4.58-4.59L10 5.75l6 6-6 6z"/><path d="M0-.25h24v24H0z" fill="none"/></svg>
          </a>
        </div>
      </div>
    </button>
  </div>
  
</div>

<style lang="scss">
  h2, h4 {
    text-transform: uppercase;
    color: hsla(0, 0%, 20%, 1);
  }

  h2 {
    font-size: 27px;
    font-weight: 500;
    letter-spacing: -0.2px;
    margin-bottom: 10px;
  }

  p, li {
    font-weight: 400;
    color: #555;
    line-height: 22px;
  }

  ul, li {
    text-decoration: none;
    list-style: disc outside;
  }

  ul {
    padding-left: 20px;
  }

  svg {
    margin: 0px;
    min-width: 24px;
    min-height: 24px;
  }

  .cards {
    margin: 0;
    width: 100vw;
    display: flex;
    align-items: center;
    justify-content: center;
    padding-bottom: 100px;

    @media only screen and (max-width: 900px) {
      flex-direction: column;
    }
  }

  .cardContainer {
    position: relative;
    width: 400px;
    height: 500px;
    min-width: 300px;
    min-height: 400px;
    margin: 4px;
    perspective: 1000px;

    @media only screen and (max-width: 900px) {
      width: 100%;
    }
  }

  .active {
    transform: translateZ(0px) rotateY(180deg) !important;
    &:after {
      display: none;
    }
  }

  .cardd {
    display: inline-block;
    width: 100%;
    height: 100%; 
    cursor: pointer;
    -moz-backface-visibility: hidden;
    transform-style: preserve-3d;
    transform: translateZ(-100px);
    transition: all 0.4s cubic-bezier(0.165, 0.84, 0.44, 1);
    &:focus {
      outline:0;
    }

    &:after {
      content: '';
      position: absolute;
      z-index: -1;
      width: 100%;
      height: 100%; 
      border-radius: 5px;
      box-shadow: 0 14px 50px -4px hsla(0, 0%, 0%, 0.15);
      opacity: 0;
      transition: all 0.6s cubic-bezier(0.165, 0.84, 0.44, 1.4);
    }

    &:hover {
      transform: translateZ(0px);
      &:hover:after {
        opacity: 1;
      }
    } 

    .side {
      -webkit-backface-visibility: hidden;
      backface-visibility: hidden;
      // position: absolute;
      width: 100%;
      height: 100%; 
      border-radius: 5px;
      background-color: hsla(0, 0%, 100%, 1);
    }

    .front {
      z-index: 2;
    }
    .back {
      transform: rotateY(180deg);
    }

    .info {
      padding: 16px;
      height: 100%;
    }
  }

  .front {
    .img {
      background-position: center;
      background-size: cover;
      border-radius: 5px 5px 0 0;
      width: 100%;
      height: 60%;
    }

    .img1 {
      background-image: url(http://i.imgur.com/1aE1nMA.jpg);
    }
    .img2 {
      background-image: url(http://i.imgur.com/2p9VXAn.jpg);
    }
    .img3 {
      background-image: url(http://i.imgur.com/I5ABT2v.jpg);
    }
  }

  .back {
    // position: relative;
    top: 0;
    position: absolute;

    h2 {
      margin-top: 6px;
      margin-bottom: 18px;
    }

    li {
      line-height: 22px;
      margin: 2px 0 6px 0;
    }

    .btn {
      position: absolute;
      bottom: 16px;
      width: calc(100% - 32px);
      height: 56px;
      display: flex;
      align-items: center;
      justify-content: center;
      background-color: #FFC324;
      background-image: linear-gradient(-90deg, #FFB714, #FFE579);
      border-radius: 5px;
      cursor: pointer;

      &:hover {
        h4 {
          transform: translateX(0px);
        }
        svg {
          transform: translateX(0px);
          opacity: 1;
        }
      }

      h4 {
        transform: translateX(12px);
        transition: transform 0.3s ease-out;
      }
      svg {
        margin: 1px 0 0 4px;
        transform: translateX(-8px);
        opacity: 0;
        transition: all 0.3s ease-out;
      }
    }
  }

</style>