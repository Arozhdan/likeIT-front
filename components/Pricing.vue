<template>
  <section class="pricing">
    <div class="container">
      <h2 class="secondary-title">Выберите подходящий План Занятий</h2>
      <div class="row pricing-inner">
        <div class="col-md-4 price-card" v-for="price in prices" :key="price.id">
          <div class="price-card-top"><span>{{price.quantity}} занятий</span></div>
          <div class="price-card-body">
            <p class="price-card-body-desc">
              <span>Запишитесь сегодня </span><br />
              и получите цену
            </p>
            <h2 class="price-card-body-amount">{{price.amount}}<span>&#8381;</span></h2>
            <ul class="price-card-body-list">
              <li class="price-card-body-list-item">
                Вечный доступ к материалам
              </li>
              <li class="price-card-body-list-item">
                Длительность урока - 1 час
              </li>
              <li class="price-card-body-list-item">
                Возможность выбрать преподавателя
              </li>
              <li class="price-card-body-list-item">
                Возможность записи урока
              </li>
            </ul>
            <div class="btn-wrapper">
              <button class="btn">Приобрести</button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
<script>
import priceQuery from '../apollo/queries/price/price.gql'
export default {
  data() {
    return {
      prices:{}
    }
  },
  apollo:{
    prices:{
      prefetch:true,
      query:priceQuery
    }
  }
  
}
</script>