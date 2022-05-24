<template>
  <div>
    <Banner />
    <Workflow />
    <CallbackSection />
    <Benefits />
    <BasicSection waved=true>
      <template>
        <div class="container">
          <h2>Бурение скважин</h2>
          <p>Команда наших профессионалов быстро и качественно выполнит самые сложные виды работ. Компактная и современная буровая установка в самые короткие сроки монтируются на участок, без повреждения ландшафта.</p>
        </div>
        <WorkDescription is-right-side=true>
          <template>
            <img src="@/assets/img/burenie.webp" alt="Фотография работающего бура">
            <p>Используемая нами установка Ураган-2 - это компактная и производительная техника, с помощью которой, мы осуществляем бурение скважин до 80 метров в глубину. Благодаря её малогабаритности, выполнение работ происходит с наибольшей точностью и аккуратностью.</p>
          </template>
        </WorkDescription>
      </template>
    </BasicSection>
  </div>
</template>

<script>
export default {
  name: 'IndexPage'
}
</script>