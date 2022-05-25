<template>
  <div id="contact" class="contact m-64">
    <div class="main">
      <h2 class="contac__theading heading">CONTACT</h2>
      <p class="contact__sub-heading sub-heading">Fan? Drop a note!</p>
      <div class="contact__content">
          <div class="contact__info col-haft col-full-mb">
            <p><i class="ti-location-pin"></i>Chicago, US</p>
            <p><i class="ti-mobile"></i>Phone:+00 151515</p>
            <p><i class="ti-email"></i>Email: mail@mail.com</p>
          </div>
          <div class="contact__form col-haft col-full-mb">
            <form action="">
              <div class="col-haft col-full-mb" style="float:left;padding-right: 8px;margin-bottom: 8px;">
                <input class="col-full" type="text" name="Name" placeholder="Name" required/>
              </div>
              <div class="col-haft col-full-mb" style="float:left;padding-left: 8px;margin-bottom: 8px;">
                <input class="col-full" type="email" name="Email" placeholder="Email" required/>
              </div>
              <div >
                <input class="col-full" type="text" name="Message" placeholder="Message" required>
              </div>
              <div>
                <button type="submit">SEND</button>
              </div>
            </form>
          </div>
        </div>
    </div>
  </div>
</template>

<style scoped>
.contact__content{
  display: flex;
  padding: 32px 0;
}
.contact__content .contact__info p{
  font-size: 18px;
  line-height: 1.6;
}
.contact__content .contact__info p i{
  padding-right: 1rem;
}
.contact__content .contact__form div input{
  line-height: 1.5;
  padding: 8px;
}
.contact__content .contact__form button{
  margin: 16px 0;
  float: right;
  background: var(--dark);
  color: var(--light);
  font-size: 15px;
  padding: 8px 13px;
  border: none;
  cursor: pointer;
}
.contact__content .contact__form button:hover{
  background: #ccc;
  color: var(--dark);
}
</style>
