<template>
  <div>
    <div class="contact-form">
      <div class="container">
        <div class="row">
          <div class="col-lg-12">
            <div class="contact__form__title">
              <h2>Add New Movie</h2>
            </div>
          </div>
        </div>
        <!-- Form Component -->
        <input-form></input-form>
      </div>
    </div>
  </div>
</template>

<script>
import InputForm from '~/components/form/InputForm.vue';

export default {
  components: {
    'input-form': InputForm
  }
}
</script>
<style>
.contact__form__title {
  margin-bottom: 50px;
  text-align: center;
}

.contact__form__title h2 {
  color: #1c1c1c;
  font-weight: 700;
}

.contact-form {
  padding-top: 80px;
  padding-bottom: 80px;
}

.contact-form form input {

  font-size: 16px;
  color: #6f6f6f;
  padding-left: 20px;
  margin-bottom: 30px;
  border: 1px solid #ebebeb;
  border-radius: 4px;
}

.contact-form form input::placeholder {
  color: #6f6f6f;
}

.contact-form form textarea {
  width: 100%;
  height: 150px;
  font-size: 16px;
  color: #6f6f6f;
  padding-left: 20px;
  margin-bottom: 24px;
  border: 1px solid #ebebeb;
  border-radius: 4px;
  padding-top: 12px;
  resize: none;
}

.contact-form form textarea::placeholder {
  color: #6f6f6f;
}

.contact-form form button {
  font-size: 18px;
  letter-spacing: 2px;
}
</style>
