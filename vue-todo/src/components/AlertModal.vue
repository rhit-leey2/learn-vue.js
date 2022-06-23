<template>
  <transition name="alertModal">
    <div class="alertModal-mask">
      <div class="alertModal-wrapper">
        <div class="alertModal-container">

          <div class="alertModal-header">
            <slot name="header">
              default header
            </slot>
          </div>

          <div class="alertModal-body">
            <slot name="body">
              default body
            </slot>
          </div>
        </div>
      </div>
    </div>
  </transition>
</template>

<style>
.alertModal-mask {
  position: fixed;
  z-index: 9998;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, .5);
  display: table;
  transition: opacity .3s ease;
}

.alertModal-wrapper {
  display: table-cell;
  vertical-align: middle;
}

.alertModal-container {
  width: 300px;
  margin: 0px auto;
  padding: 20px 30px;
  background-color: #fff;
  border-radius: 2px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, .33);
  transition: all .3s ease;
  font-family: Helvetica, Arial, sans-serif;
}

.alertModal-header h3 {
  margin-top: 0;
  color: #42b983;
}

.alertModal-body {
  margin: 20px 0;
}

.alertModal-default-button {
  float: right;
}

/*
 * The following styles are auto-applied to elements with
 * transition="alertModal" when their visibility is toggled
 * by Vue.js.
 *
 * You can easily play with the alertModal transition by editing
 * these styles.
 */


.alertModal-enter {
  opacity: 0;
}

.alertModal-leave-active {
  opacity: 0;
}

.alertModal-enter .alertModal-container,
.alertModal-leave-active .alertModal-container {
  -webkit-transform: scale(1.1);
  transform: scale(1.1);
}
</style>
