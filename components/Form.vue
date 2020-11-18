<template>
  <section class="contacts-form">
    <div class="container">
      <div class="contact-form-inner">
        <div class="contact-form-left">
          <form class="contact-form-body">
            <div class="form-group">
              <label for="student_name">Возраст и Имя ребенка</label>
              <input
                type="text"
                id="student_name"
                placeholder="Возраст и Имя ребенка"
              />
            </div>
            <div class="form-group">
              <label for="parent_name">Имя и Отчество родителя</label>
              <input
                type="text"
                id="parent_name"
                placeholder="Имя и Отчество родителя"
              />
            </div>
            <div class="form-group">
              <label for="contact_number">Телефон родителя</label>
              <input
                type="text"
                id="contact_number"
                placeholder="Телефон родителя"
              />
            </div>
            <div class="form-group form-checked">
              <input type="checkbox" id="confid" name="confid" required />
              <label class="checkbox-label" for="confid"
                >Принимаю условия <a href="#">соглашения</a> и
                <a href="#"> политики конфиденциальности</a>
              </label>
            </div>
            <div class="btn-wrapper">
              <button class="btn btn__submit">Оставить заявку</button>
            </div>
          </form>
        </div>
        <div class="contact-form-right">
          <h3 class="contact-form-right-title">Остались вопросы?</h3>
          <ul class="contact-form-right-steps-wrapper">
            <li class="contact-form-right-steps contact-form-right-steps__bold">
              Оставьте заявку
            </li>
            <li class="contact-form-right-steps">
              Наш менеджер позвонит Вам с 9:00 до 21:00 по МСК или на следующий
              день, если заявка отправлена в ночное время
            </li>
            <li class="contact-form-right-steps">
              Менеджер ответит на все Ваши вопросы, ппожберет оптимальный план
              обучения и назначит вводное занятие
            </li>
          </ul>
        </div>
      </div>
    </div>
  </section>
</template>