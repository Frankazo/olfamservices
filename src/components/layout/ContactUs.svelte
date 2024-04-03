<script>
  let checked = false;
</script>

<form class="my-form" id="contact" method="POST" data-netlify="true"> 
    <div class="container">
      <h1>Request a Quote or Get in touch!</h1>
      <ul>
        <li>
          <select>
            <option selected disabled>Please choose an option:</option>
            <option>Request Quote</option>
            <option>Question about services</option>
            <option>Other</option>
          </select>
        </li>
        <li>
          <select>
            <option selected disabled>Selects Services:</option>
            <option value="Wood and Metal Framing">Wood and Metal Framing</option>
            <option value="Moulding & Millwork">Moulding & Millwork</option>
            <option value="Window">Window Installation</option>
            <option value="Door">Doors and Sliding Doors Installations</option>
            <option value="Demolition">Demolition</option>
            <option value="Multiple">Multiple services (please describe)</option>
            <option value="Other">Other (please describe)</option>
          </select>
        </li> 
        <li>
          <div class="grid grid-2">
            <input type="text" placeholder="Name" required>
            <input type="tel" placeholder="Phone">
          </div>
        </li>
        <li>
          <div class="grid grid-2">
            <input type="email" placeholder="Email" required>  
            <input type="address" placeholder="Address">
          </div>
        </li>   
        <li>
          <textarea placeholder="Message"></textarea>
        </li>   
        <li>
          <input type="checkbox" id="terms" bind:checked={checked}>
          <label for="terms">I have read and agreed with <a href="#terms">the terms and conditions.</a></label>
        </li>  
        <li>
          <div class="grid grid-2">
            <div class="required-msg">REQUIRED FIELDS</div>
            <button class="btn-grid" type="submit" disabled={!checked}>
              <span class="back">
                <img src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/162656/email-icon.svg" alt="">
              </span>
              <span class="front">SUBMIT</span>
            </button>
            <!-- <button class="btn-grid" type="reset" disabled={!checked}>
              <span class="back">
                <img src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/162656/eraser-icon.svg" alt="">
              </span>
              <span class="front">RESET</span>
            </button>  -->
          </div>
        </li>    
      </ul>
    </div>
</form>

<style lang="scss">
  form {
    padding: 200px 0;
  }

  a {
    color: inherit;
  }

  input,
  select,
  textarea,
  button {
    font-family: inherit;
    font-size: 100%;
  }

  button,
  label {
    cursor: pointer;
    color: #afafaf;
  }

  select {
    appearance: none;
  }

  /* Remove native arrow on IE */
  select::-ms-expand {
    display: none;
  }

  /*Remove dotted outline from selected option on Firefox*/
  /*https://stackoverflow.com/questions/3773430/remove-outline-from-select-box-in-ff/18853002#18853002*/
  /*We use !important to override the color set for the select on line 99*/
  select:-moz-focusring {
    color: transparent !important;
    text-shadow: 0 0 0 #afafaf;
  }

  textarea {
    resize: none;
  }

  ul {
    list-style: none;
    width: 100%;
  }

  .container {
    margin: 0 auto;
    padding: 0 1.5rem;

    display: flex;
    max-width: 1200px;
    justify-content: center;
    gap: 50px;
    align-items: baseline;
  }


  /* FORM ELEMENTS
  –––––––––––––––––––––––––––––––––––––––––––––––––– */
  .my-form h1 {
    margin-bottom: 1.5rem;
    color: #afafaf;
    max-width: 400px;
    color: #000;
    font-size: 3rem;
  }

  .my-form li,
  .my-form .grid > *:not(:last-child) {
    margin-bottom: 1.5rem;
  }

  .my-form select,
  .my-form input,
  .my-form textarea,
  .my-form button {
    width: 100%;
    line-height: 1.5;
    padding: 15px 10px;
    border: 1px solid hsl(0, 0%, 10%);
    color: #afafaf;
    background: hsl(0, 0%, 14%);
    transition: background-color 0.3s cubic-bezier(0.57, 0.21, 0.69, 1.25),
      transform 0.3s cubic-bezier(0.57, 0.21, 0.69, 1.25);
  }

  .my-form textarea {
    height: 170px;
  }

  .my-form ::placeholder {
    color: inherit;
    /*Fix opacity issue on Firefox*/
    opacity: 1;
  }

  .my-form select:focus,
  .my-form input:focus,
  .my-form textarea:focus,
  .my-form button:enabled:hover,
  .my-form button:focus,
  .my-form input[type="checkbox"]:focus + label {
    background: hsl(0, 7%, 20%);
  }

  .my-form select:focus,
  .my-form input:focus,
  .my-form textarea:focus {
    transform: scale(1.02);
  }

  .my-form *:required,
  .my-form select {
    background-repeat: no-repeat;
    background-position: center right 12px;
    background-size: 15px 15px;
  }

  .my-form *:required {
    background-image: url(https://s3-us-west-2.amazonaws.com/s.cdpn.io/162656/asterisk.svg);  
  }

  .my-form select {
    background-image: url(https://s3-us-west-2.amazonaws.com/s.cdpn.io/162656/down.svg);
  }

  .my-form *:disabled {
    cursor: default;
    filter: blur(2px);
    background-color: #000;
  }


  /* FORM BTNS
  –––––––––––––––––––––––––––––––––––––––––––––––––– */
  .my-form .required-msg {
    display: none;
    background: url(https://s3-us-west-2.amazonaws.com/s.cdpn.io/162656/asterisk.svg)
      no-repeat center left / 15px 15px;
    padding-left: 20px;
    color: #afafaf;
  }

  .my-form .btn-grid {
    position: relative;
    overflow: hidden;
    transition: filter 0.2s, background-color 0.2s;
  }

  .my-form button {
    font-weight: bold;
  }

  .my-form button > * {
    display: inline-block;
    width: 100%;
    transition: transform 0.4s ease-in-out;
  }

  .my-form button .back {
    position: absolute;
    left: 50%;
    top: 50%;
    transform: translate(-110%, -50%);
  }

  .my-form button:enabled:hover .back,
  .my-form button:focus .back {
    transform: translate(-5%, -50%);
  }

  .my-form button:enabled:hover .front,
  .my-form button:focus .front {
    transform: translateX(110%);
  }


  /* CUSTOM CHECKBOX
  –––––––––––––––––––––––––––––––––––––––––––––––––– */
  .my-form input[type="checkbox"] {
    position: absolute;
    left: -9999px;
  }

  .my-form input[type="checkbox"] + label {
    position: relative;
    display: inline-block;
    padding-left: 2rem;
    transition: background-color 0.3s cubic-bezier(0.57, 0.21, 0.69, 1.25);
  }

  .my-form input[type="checkbox"] + label::before,
  .my-form input[type="checkbox"] + label::after {
    content: '';
    position: absolute;
  }

  .my-form input[type="checkbox"] + label::before {
    left: 0;
    top: 6px;
    width: 18px;
    height: 18px;
    border: 2px solid #afafaf;
  }

  .my-form input[type="checkbox"]:checked + label::before {
    background-color: #e31b23;
  }

  .my-form input[type="checkbox"]:checked + label::after {
    left: 7px;
    top: 7px;
    width: 6px;
    height: 14px;
    border-bottom: 2px solid #afafaf;
    border-right: 2px solid #afafaf;
    transform: rotate(45deg);
  }

  /* MQ
  –––––––––––––––––––––––––––––––––––––––––––––––––– */


  @media screen and (max-width: 767px) {
    form {
      padding: 100px 0;

      .container {
        flex-direction: column;
      }

      h1 {
        line-height: 40px;
      }
    }
  }
  @media screen and (min-width: 600px) {
    .my-form .grid {
      display: grid;
      grid-gap: 1.5rem;
      align-items: center;
    }

    .my-form .grid-2 {
      grid-template-columns: 1fr 1fr;
    }

    .my-form .grid > *:not(:last-child) {
      margin-bottom: 0;
    }

    .my-form .required-msg {
      display: block;
    }
  }

  @media screen and (min-width: 541px) {
    .my-form input[type="checkbox"] + label::before {
      top: 50%;
      transform: translateY(-50%);
    }

    .my-form input[type="checkbox"]:checked + label::after {
      top: 3px;
    }
  }
</style>