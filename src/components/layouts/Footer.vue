<template lang="">
  <footer class="footer">
        <p>2023 - Todos os direitos reservados | CNPJ: 00.000.000/0000-00 BIRIGUI - SP</p>
        <img src="@/assets/images/logo.jpg" alt="">
      </footer>
</template>
<script>
export default {
  name: 'Footer'
}
</script>
<style>
.footer {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  margin: 60px;
  text-align: center;
}

.footer p {
  font-size: .8rem;
  color: var(--text-color2);
  margin-bottom: 10px;
}

.footer img {
  width: 10%;
}

@media screen and (max-width: 1023px) {
  .footer img {
    width: 60%;
  }
}
</style>