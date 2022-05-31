<template>
    <ul class="about">
        <li class="about__element">
            <WorkElement image="burenie" text="Бурение скважин на воду"/>
        </li>
        <li class="about__element">
            <WorkElement image="automation" text="Обустройство скважин"/>
        </li>
        <li class="about__element">
            <WorkElement image="automation2" text="Автоматизация скважин"/>
        </li>
        <li class="about__element">
            <WorkElement image="teplypol" text="Обустройство систем отопления и тёплых полов"/>
        </li>
        <li class="about__element">
            <WorkElement image="kanalizaciya" text="Обустройство систем водоснабжения и канализации"/>
        </li>
    </ul>
</template>

<style lang="scss" scoped>
.about {
    display: flex;
    justify-content: space-between;
    margin-bottom: 30px;
    flex-wrap: wrap;

        @media screen and (max-width:$MEDIA_DESKTOP_TO_TABLET) {
            justify-content: center;
            gap: 40px;
        }

        @media screen and (max-width:$MEDIA_TABLET_TO_BIG_MOBILE) {
            gap: 20px;
            justify-content: space-around;
        }

    &__element {
        max-width: 18%;

        @media screen and (max-width:$MEDIA_DESKTOP_TO_TABLET) {
            max-width: 30%;
        }

        @media screen and (max-width:$MEDIA_TABLET_TO_BIG_MOBILE) {
            max-width: unset;
            width: calc(50% - 10px);
        }
    }
}
</style>