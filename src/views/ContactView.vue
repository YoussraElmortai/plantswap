<script>
export default {
  data() {
    return {
      status: '',
      form: {
        name: '',
        lastname: '',
        email: '',
        message: '',
      },
    }
  },
  methods: {
    async handleSubmit(event) {
      this.status = 'Submitting...'
      const formData = new FormData(event.target)
      const object = Object.fromEntries(formData)
      const json = JSON.stringify(object)

      try {
        const response = await fetch('https://api.web3forms.com/submit', {
          method: 'POST',
          headers: {
            'Content-Type': 'application/json',
            Accept: 'application/json',
          },
          body: json,
        })
        const result = await response.json()
        if (result.success) {
          console.log(result)
          this.status = result.message || 'Success'
          // Reset form after successful submission
          this.form = {
            name: '',
            lastname: '',
            email: '',
            message: '',
          }
        }
      } catch (error) {
        this.status = 'Error submitting form'
        console.error(error)
      }
    },
  },
}
</script>

<template>
  <section class="intro">
    <h1>Contact</h1>
    <p>
      Questions, suggestions, or just in the mood for a green chat? Get in touch, and let's talk
      plants!
    </p>
  </section>
  <section class="contact_content">
    <div class="form">
      <h2>Get in touch</h2>
      <form @submit.prevent="handleSubmit" class="contact">
        <input type="hidden" name="access_key" value="" />
        <div>
          <input
            type="text"
            name="name"
            v-model="form.name"
            placeholder="Your Name"
            class="contact_inputs"
            required
          />
          <input
            type="text"
            name="lastname"
            v-model="form.lastname"
            placeholder="Lastname"
            class="contact_inputs"
            required
          />
        </div>
        <input
          type="email"
          name="email"
          v-model="form.email"
          placeholder="Your email"
          class="contact_inputs"
          required
        />
        <textarea
          name="message"
          v-model="form.message"
          placeholder="Your Message"
          class="contact_inputs"
          required
        ></textarea>
        <button class="link_secondary" type="submit">Submit</button>
        <p v-if="status">{{ status }}</p>
      </form>
    </div>

    <div>
      <iframe
        src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2436.673597778716!2d4.923641976905991!3d52.35820497201926!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x47c6097132bffcc7%3A0x290544c1d1a9e37c!2sOBA%20Linnaeus!5e0!3m2!1snl!2snl!4v1744629094124!5m2!1snl!2snl"
        width="400"
        height="300"
        style="border: 0; border-radius: 0.5rem"
        loading="lazy"
        referrerpolicy="no-referrer-when-downgrade"
      ></iframe>
    </div>
  </section>
</template>

<style scoped>
.contact_content {
  display: flex;
  flex-flow: row wrap;
  gap: 2rem;
  justify-content: space-between;
}

.form {
  display: flex;
  flex-flow: column;
}
.contact {
  display: flex;
  flex-flow: column;
  max-width: 30rem;
  gap: 0.5rem;

  & div {
    display: flex;
    flex-flow: row wrap;
    gap: 0.5rem;
    width: 100%;

    & input {
      flex: 1;
      min-width: 0;
    }
  }

  & input,
  textarea {
    border: solid var(--bg-color);
    padding: 0.5rem 1rem;
    border-radius: 0.5rem;
  }

  & textarea {
    min-height: 70px;
    max-height: 120px;
    max-width: 100%;
  }

  & button {
    width: fit-content;
    align-self: flex-end;
    margin-top: 1rem;
  }
}

.contact_inputs {
  &:focus {
    border: solid var(--accent-color);
  }

  &::placeholder {
    color: #585858;
  }
}
</style>
