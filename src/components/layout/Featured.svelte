<script>
    const cards = document.querySelectorAll('.card');

    function transition() {
    if (this.classList.contains('active')) {
        this.classList.remove('active')
    } else {
        this.classList.add('active');
    }
    }

    cards.forEach(card => card.addEventListener('click', transition));
</script>

<div class="cardContainer inactive">
    <div class="card">
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
          <div class="reviews">
            <svg fill="#FFC324" height="24" viewBox="0 0 24 24" width="24" xmlns="http://www.w3.org/2000/svg"><path d="M0 0h24v24H0z" fill="none"/><path d="M12 17.27L18.18 21l-1.64-7.03L22 9.24l-7.19-.61L12 2 9.19 8.63 2 9.24l5.46 4.73L5.82 21z"/><path d="M0 0h24v24H0z" fill="none"/></svg>
            <svg fill="#FFC324" height="24" viewBox="0 0 24 24" width="24" xmlns="http://www.w3.org/2000/svg"><path d="M0 0h24v24H0z" fill="none"/><path d="M12 17.27L18.18 21l-1.64-7.03L22 9.24l-7.19-.61L12 2 9.19 8.63 2 9.24l5.46 4.73L5.82 21z"/><path d="M0 0h24v24H0z" fill="none"/></svg>
            <svg fill="#FFC324" height="24" viewBox="0 0 24 24" width="24" xmlns="http://www.w3.org/2000/svg"><path d="M0 0h24v24H0z" fill="none"/><path d="M12 17.27L18.18 21l-1.64-7.03L22 9.24l-7.19-.61L12 2 9.19 8.63 2 9.24l5.46 4.73L5.82 21z"/><path d="M0 0h24v24H0z" fill="none"/></svg>
            <svg fill="#FFC324" height="24" viewBox="0 0 24 24" width="24" xmlns="http://www.w3.org/2000/svg"><path d="M0 0h24v24H0z" fill="none"/><path d="M12 17.27L18.18 21l-1.64-7.03L22 9.24l-7.19-.61L12 2 9.19 8.63 2 9.24l5.46 4.73L5.82 21z"/><path d="M0 0h24v24H0z" fill="none"/></svg>
            <svg fill="#FFC324" height="24" viewBox="0 0 24 24" width="24" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink">
              <defs><path d="M0 0h24v24H0V0z" id="a"/></defs><clipPath id="b"><use overflow="visible" xlink:href="#a"/></clipPath><path clip-path="url(#b)" d="M22 9.24l-7.19-.62L12 2 9.19 8.63 2 9.24l5.46 4.73L5.82 21 12 17.27 18.18 21l-1.63-7.03L22 9.24zM12 15.4V6.1l1.71 4.04 4.38.38-3.32 2.88 1 4.28L12 15.4z"/>
            </svg>
            <p>23 Reviews</p>
          </div>
          <ul>
            <li>Manage backyard gates with ease with the 36" deck option</li>
            <li>Your choice of deck sizes ranging from 36", 48", 52" and 60"</li>
            <li>Updated hip bolstering offers superior operator comfort and positioning</li>
          </ul>
          <div class="btn">
            <h4>Learn More</h4>
            <svg fill="#333" height="24" viewBox="0 0 24 24" width="24" xmlns="http://www.w3.org/2000/svg"><path d="M8.59 16.34l4.58-4.59-4.58-4.59L10 5.75l6 6-6 6z"/><path d="M0-.25h24v24H0z" fill="none"/></svg>
          </div>
        </div>
      </div>
    </div>
  </div>
  
  <div class="cardContainer inactive">
    <div class="card">
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
          <div class="reviews">
            <svg fill="#FFC324" height="24" viewBox="0 0 24 24" width="24" xmlns="http://www.w3.org/2000/svg"><path d="M0 0h24v24H0z" fill="none"/><path d="M12 17.27L18.18 21l-1.64-7.03L22 9.24l-7.19-.61L12 2 9.19 8.63 2 9.24l5.46 4.73L5.82 21z"/><path d="M0 0h24v24H0z" fill="none"/></svg>
            <svg fill="#FFC324" height="24" viewBox="0 0 24 24" width="24" xmlns="http://www.w3.org/2000/svg"><path d="M0 0h24v24H0z" fill="none"/><path d="M12 17.27L18.18 21l-1.64-7.03L22 9.24l-7.19-.61L12 2 9.19 8.63 2 9.24l5.46 4.73L5.82 21z"/><path d="M0 0h24v24H0z" fill="none"/></svg>
            <svg fill="#FFC324" height="24" viewBox="0 0 24 24" width="24" xmlns="http://www.w3.org/2000/svg"><path d="M0 0h24v24H0z" fill="none"/><path d="M12 17.27L18.18 21l-1.64-7.03L22 9.24l-7.19-.61L12 2 9.19 8.63 2 9.24l5.46 4.73L5.82 21z"/><path d="M0 0h24v24H0z" fill="none"/></svg>
            <svg fill="#FFC324" height="24" viewBox="0 0 24 24" width="24" xmlns="http://www.w3.org/2000/svg"><path d="M0 0h24v24H0z" fill="none"/><path d="M12 17.27L18.18 21l-1.64-7.03L22 9.24l-7.19-.61L12 2 9.19 8.63 2 9.24l5.46 4.73L5.82 21z"/><path d="M0 0h24v24H0z" fill="none"/></svg>
            <svg fill="#FFC324" height="24" viewBox="0 0 24 24" width="24" xmlns="http://www.w3.org/2000/svg"><path d="M0 0h24v24H0z" fill="none"/><path d="M12 17.27L18.18 21l-1.64-7.03L22 9.24l-7.19-.61L12 2 9.19 8.63 2 9.24l5.46 4.73L5.82 21z"/><path d="M0 0h24v24H0z" fill="none"/></svg>
            <p>39 Reviews</p>
          </div>
          <ul>
            <li>Your choice of VX4 decks ranging from 60 to 72 inches</li>
            <li>The 37hp Vanguard BigBlock EFI makes short work out of big jobs enabling speeds up to 16mph</li>
            <li>Massive 24" drive tires and 13" front caster tires</li>
          </ul>
          <div class="btn">
            <h4>Learn More</h4>
            <svg fill="#333" height="24" viewBox="0 0 24 24" width="24" xmlns="http://www.w3.org/2000/svg"><path d="M8.59 16.34l4.58-4.59-4.58-4.59L10 5.75l6 6-6 6z"/><path d="M0-.25h24v24H0z" fill="none"/></svg>
          </div>
        </div>
      </div>
    </div>
  </div>
  
  <div class="cardContainer inactive">
    <div class="card">
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
          <div class="reviews">
            <svg fill="#FFC324" height="24" viewBox="0 0 24 24" width="24" xmlns="http://www.w3.org/2000/svg"><path d="M0 0h24v24H0z" fill="none"/><path d="M12 17.27L18.18 21l-1.64-7.03L22 9.24l-7.19-.61L12 2 9.19 8.63 2 9.24l5.46 4.73L5.82 21z"/><path d="M0 0h24v24H0z" fill="none"/></svg>
            <svg fill="#FFC324" height="24" viewBox="0 0 24 24" width="24" xmlns="http://www.w3.org/2000/svg"><path d="M0 0h24v24H0z" fill="none"/><path d="M12 17.27L18.18 21l-1.64-7.03L22 9.24l-7.19-.61L12 2 9.19 8.63 2 9.24l5.46 4.73L5.82 21z"/><path d="M0 0h24v24H0z" fill="none"/></svg>
            <svg fill="#FFC324" height="24" viewBox="0 0 24 24" width="24" xmlns="http://www.w3.org/2000/svg"><path d="M0 0h24v24H0z" fill="none"/><path d="M12 17.27L18.18 21l-1.64-7.03L22 9.24l-7.19-.61L12 2 9.19 8.63 2 9.24l5.46 4.73L5.82 21z"/><path d="M0 0h24v24H0z" fill="none"/></svg>
            <svg fill="#FFC324" height="24" viewBox="0 0 24 24" width="24" xmlns="http://www.w3.org/2000/svg"><path d="M0 0h24v24H0z" fill="none"/><path d="M12 17.27L18.18 21l-1.64-7.03L22 9.24l-7.19-.61L12 2 9.19 8.63 2 9.24l5.46 4.73L5.82 21z"/><path d="M0 0h24v24H0z" fill="none"/></svg>
            <svg fill="#FFC324" height="24" viewBox="0 0 24 24" width="24" xmlns="http://www.w3.org/2000/svg"><path d="M22 9.24l-7.19-.62L12 2 9.19 8.63 2 9.24l5.46 4.73L5.82 21 12 17.27 18.18 21l-1.63-7.03L22 9.24zM12 15.4l-3.76 2.27 1-4.28-3.32-2.88 4.38-.38L12 6.1l1.71 4.04 4.38.38-3.32 2.88 1 4.28L12 15.4z"/><path d="M0 0h24v24H0z" fill="none"/></svg>
            <p>26 Reviews</p>
          </div>
          <ul>
            <li>V-Twin OHV Technology provides superior balance, low vibration, lower emissions, better fuel economy and higher HP/Weight</li>
            <li>Advanced Debris Management keeps engine clean and cool for enhanced durability and performance</li>
          </ul>
          <div class="btn">
            <h4>Learn More</h4>
            <svg fill="#333" height="24" viewBox="0 0 24 24" width="24" xmlns="http://www.w3.org/2000/svg"><path d="M8.59 16.34l4.58-4.59-4.58-4.59L10 5.75l6 6-6 6z"/><path d="M0-.25h24v24H0z" fill="none"/></svg>
          </div>
        </div>
      </div>
    </div>
  </div>
  

<style lang="scss">
    .cardContainer{
        position: relative;
        //   +size(300px, 400px)
        min-width: 300px;
        min-height: 400px;
        margin: 4px;
        perspective: 1000px;
    }

    // .active is applied to .card when .card is clicked.
    .active {
    transform: translateZ(0px) rotateY(180deg) !important;
    &:after {
        display: none
    }
    }

.card {
  display: inline-block;
//   +size(100%, 100%);
  cursor: pointer;
  -moz-backface-visibility: hidden;
  transform-style: preserve-3d;
  transform: translateZ(-100px);
  transition: all 0.4s cubic-bezier(0.165, 0.84, 0.44, 1);

  // :after allows for a more performant box-shadow because only opacity is being animated.
  &:after {
    content: '';
    position: absolute;
    z-index: -1;
    // +size(100%, 100%);
    border-radius: 5px;
    box-shadow: 0 14px 50px -4px hsla(0, 0%, 0%, 0.15);
    opacity: 0;
    transition: all 0.6s cubic-bezier(0.165, 0.84, 0.44, 1.4);
  }
  &:hover {
    transform: translateZ(0px);
  }
  &:hover:after {
    opacity: 1;
  }

  .side {
    -webkit-backface-visibility: hidden;
    backface-visibility: hidden;
    position: absolute;
    // +size(100%, 100%);
    border-radius: 5px;
    background-color: $l1;
  }

  .front {
    z-index: 2;
  }
  .back {
    transform: rotateY(180deg);
  }

  .info {
    padding: 16px;
  }

}

// --------------
// Front of card
// --------------

.front {
  .img {
    background-color: $l2;
    background-position: center;
    background-size: cover;
    border-radius: 5px 5px 0 0;
    // +size(100%, 250px);
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



// --------------
// Back of card
// --------------

.back {
  position: relative;

    h2 {
    margin-top: 6px;
    margin-bottom: 18px;
    }

    .reviews {
        display: flex;
        align-items: center;
        margin-bottom: 12px;
        cursor: pointer;

        p {
            color: $l3;
            font-weight: 300;
            margin: 1px 0 0 6px;
            transition: 0.3s ease-in-out;
        }

        &:hover {
            p {
                color: $d2;
            }
        }
    }

    li {
        line-height: 22px;
        margin: 2px 0 6px 0;
    }

    .btn {
        // positioning;
        position: absolute;
        bottom: 16px;
        // +size(calc(100% - 32px), 56px);
        display: flex;
        align-items: center;
        justify-content: center;
        // style
        background-color: $p1;
        background-image: linear-gradient(-90deg, $g1, $g2);
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