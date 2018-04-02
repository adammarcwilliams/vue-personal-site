<template>
  <div class="title-card">
    <div class="name">{{ name }}</div>
    <div class="role">{{ role }}</div>
    <div class="company">@{{ company }}</div>
  </div>
</template>

<script>
export default {
  name: 'TitleCard',
  data () {
    return {
      name: 'Adam Marc Williams',
      role: 'Interactive Developer',
      company: 'Rhythm Digital'
    }
  }
}
</script>

<style lang='scss' scoped>
@import '../assets/scss/index.scss';

.title-card {
  position: relative;
  width: 290px;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: flex-end;
  color: $light-copy;
  font-family: $ptsans;
  margin-right: 40px;
}

.name {
  font-family: $oswald;
  font-size: 30px;
}

.role {
  font-size: 24px;
  margin-top: 5px;
}

.company {
  font-size: 20px;
  margin-top: 5px;
}

</style>
