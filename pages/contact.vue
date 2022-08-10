<template>
  <div>
    <div>
      <Header />
    </div>
    <div class="container">
      <div class="contact-box">
        <h2 class="contact-title">Contact</h2>

        <div class="contact-fields">
          <div class="contact-name">
            <label for="name">Name</label>
            <input type="text" id="name" />
          </div>
          <div class="contact-email">
            <label for="email">Email</label>
            <input type="email" id="email" />
          </div>
          <div class="contact-message">
            <label for="message">Message</label>
            <textarea id="message"></textarea>
          </div>
        </div>
        <div class="box-actions">
          <button class="action-button">Send</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped lang="scss">
.container {
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  position: absolute;
}

.contact-box {
  height: 396px;
  width: 396px;
  background-color: rgb(238, 238, 238);
  border-radius: 16px;

  .contact-title {
    position: absolute;
    margin: 16px;
  }

  .contact-fields {
    position: absolute;
    top: 50%;
    left: 29%;
    transform: translate(-50%, -50%);
    width: 100%;
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;

    font-family: "Nunito", sans-serif;
    input[type="text"],
    input[type="email"] {
      outline: none;
      border: none;
      background-color: rgb(219, 219, 219);
      border-radius: 4px;
      padding: 10px 12px;
      margin-bottom: 32px;

      transition: border-bottom 0.2s ease-in-out;

      &:focus {
        border-bottom: 1px solid #feb65e;
      }
    }

    textarea {
      outline: none;
      border: none;
      font-family: "Nunito", sans-serif;
      background-color: rgb(219, 219, 219);
      border-radius: 4px;
      padding: 12px 20px;
      margin-bottom: 32px;
      resize: none;

      transition: border-bottom 0.2s ease-in-out;
      &:focus {
        border-bottom: 1px solid #feb65e;
      }
    }

    label {
      display: block;
      font-size: 15px;
      font-weight: bold;
      color: black;
    }
  }

  .box-actions {
    position: absolute;
    top: 96%;
    left: 89%;
    transform: translate(-50%, -50%);
    width: 100%;
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .action-button {
    outline: none;
    border: none;
    font-family: "Nunito", sans-serif;
    font-weight: 600;
    background-color: #feb65e;
    color: white;
    border-radius: 4px;
    padding: 10px 12px;
    margin-bottom: 32px;
    cursor: pointer;
    transition: background-color 0.2s ease-in-out;
  }

  ::-webkit-scrollbar {
    width: 8px;
  }

  /* Track */
  ::-webkit-scrollbar-track {
    background-color: rgb(180, 180, 180);
    border-radius: 10px;
  }

  /* Handle */
  ::-webkit-scrollbar-thumb {
    background: rgb(141, 141, 141);
    border-radius: 10px;
  }
}
</style>
