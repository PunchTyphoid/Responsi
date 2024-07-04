<template>
  <link rel='stylesheet' href='https://cdn.jsdelivr.net/npm/bootstrap@4.4.1/dist/css/bootstrap.min.css'>
  <section class="contact">
    <div class="container">
    <h2>Contact Me</h2>
    <form  @submit.prevent="sendMessage">
      <div class="mb-3">
        <label for="exampleInputEmail1" class="form-label">Email address</label>
        <input type="email" class="form-control" id="exampleInputEmail1" aria-describedby="emailHelp">
      </div>
      <div class="mb-3">
        <label for="exampleInputPassword1" class="form-label">Subject</label>
        <input type="text" class="form-control" id="exampleInputPassword1">
      </div>
      <button type="submit" class="btn btn-primary">Submit</button>
  </form>
    <div v-if="success" class="success-message">
      Pesan Anda telah terkirim! Terima kasih.
    </div>
    <div v-if="error" class="error-message">
      Terjadi kesalahan saat mengirim pesan. Silakan coba lagi.
    </div>
  </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      name: '',
      email: '',
      message: '',
      success: false,
      error: false,
    };
  },
  methods: {
    async sendMessage() {
      try {
        // Kirimkan data form ke backend Anda di sini
        // Contoh menggunakan Axios
        const response = await axios.post('/api/contact', {
          name: this.name,
          email: this.email,
          message: this.message,
        });

        if (response.status === 200) {
          this.success = true;
          this.error = false;
        } else {
          this.error = true;
          this.success = false;
        }
      } catch (error) {
        this.error = true;
        this.success = false;
        console.error(error);
      } finally {
        // Reset form setelah terkirim
        this.name = '';
        this.email = '';
        this.message = '';
      }
    },
  },
};
</script>

<style scoped>
h2{
  text-align: center;
}

.container{
  width: 70%;
  margin: 0 auto;
  background-color: #ffffff;
}
.contact-form {
  max-width: 600px;
  margin: 0 auto;
  padding: 20px;
  background-color: #ffffff;
  border-radius: 5px;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
}

.form-group {
  margin-bottom: 15px;
}

label {
  display: block;
  margin-bottom: 5px;
}

input,
textarea {
  width: 100%;
  padding: 10px;
  border: 1px solid #000000;
  border-radius: 3px;
}

button {
  background-color: #4CAF50;
  color: #000000;
  padding: 10px 20px;
  border: none;
  border-radius: 3px;
  cursor: pointer;
}

.success-message,
.error-message {
  padding: 10px;
  border-radius: 3px;
  margin-top: 15px;
}

.success-message {
  background-color: #4CAF50;
  color: #ffffff;
}

.error-message {
  background-color: #f44336;
  color: #ffffff;
}
</style>