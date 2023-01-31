<template>
  <div class="wrapper">
    <img
      src="../assets/img/collection/contact.jpg"
      alt=""
      class="contact-img"
    />
    <div class="d-flex align-items-center justify-content-center pb-5">
      <div class="contact-box mr-3 d-flex flex-column justify-content-center">
        <div class="img-contact">
          <i class="fa-solid fa-mobile-screen-button icon-contact"></i>
        </div>
        <div class="body-contact">
          <div class="heading-contact ml-4 mb-3">Liên lạc</div>
          <div class="phone-body ml-2">+8465121259</div>
          <div class="mail-body">info@bikeshop.com</div>
        </div>
      </div>
      <div class="contact-box mr-3 d-flex flex-column justify-content-center">
        <div class="img-contact">
          <i class="fa-solid fa-people-arrows icon-contact"></i>
        </div>
        <div class="body-contact">
          <div class="heading-contact ml-4 mb-3">Theo dõi chúng tôi</div>
          <div class="social d-flex">
            <div class="fb-social">facebook</div>
            <div class="youtube-social">youtube</div>
            <div class="ins-social">instagram</div>
          </div>
        </div>
      </div>
      <div class="contact-box mr-3 d-flex flex-column justify-content-center">
        <div class="img-contact">
          <i class="fa-regular fa-address-book icon-contact"></i>
        </div>
        <div class="body-contact">
          <div class="heading-contact ml-4 mb-3">Địa chỉ</div>
          <div class="ml-2" style="font-size: 12px">
            Hẻm 51 đường 3/2 quận Ninh Kiều phường Hưng Lợi tp Cần Thơ
          </div>
        </div>
      </div>
      <div class="contact-box mr-3 d-flex flex-column justify-content-center">
        <div class="img-contact">
          <i class="fa-solid fa-mobile-screen-button icon-contact"></i>
        </div>
        <div class="body-contact">
          <div class="heading-contact ml-4 mb-3">Thanh toán</div>
          <div class="ml-2">Số tk : 8465121259</div>
          <div class="mt-2" style="font-size: 12px">
            Ngân hàng : Sacombank chi nhánh An Giang
          </div>
          <div class="mt-2" style="font-size: 12px">
            Chủ sở hữu : Huỳnh Đại Huy
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<style scoped>
.wrapper {
  margin-top: 78px;
  width: 100%;
  min-height: 50vh;
  background: black;
}
.contact-img {
  width: 100%;
  height: 100%;
  object-fit: contain;
}

.contact-box {
  background-color: aqua;
  padding: 4rem;
  background: #fff;
  border-radius: 4px;
  border: 0.1rem solid #e1e1e1;
  position: relative;
  width: 280px;
  height: 240px;
  box-shadow: 0 3px 10px rgba(0, 0, 0, 0.2);
}
.contact-box:hover {
  cursor: pointer;
  transform: translateY(-4px);
  transition: all linear 0.2s;
}
.icon-contact {
  position: absolute;
  top: -24%;
  left: 33%;
  font-size: 40px;
  padding: 30px;
  border-radius: 50%;
  background: #fff;
}
.heading-contact {
  font-size: 16px;
  font-weight: 550;
}
.social {
  gap: 8px;
}
.social > div {
  font-size: 12px;
}
</style>