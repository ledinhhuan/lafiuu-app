<template>
  <div class="authenticate-wrapper">
    <div class="container">
      <div class="authenticate-outer">
        <div class="authenticate-inner">
          <div class="authenticate">
            <div class="authenticate__header">
              <img
                src="~@/assets/logo/logo-blue.svg"
                alt="Lafiuu Logo"
                class="authenticate__logo"
              />
              <h1 class="authenticate__title">Welcome to Lafyuu</h1>
              <p class="authenticate__desc">Sign in to continue</p>
            </div>
            <div class="authenticate__body">
              <div class="form-authenticate">
                <div class="input-wrapper">
                  <input
                    type="text"
                    placeholder="Your Email"
                    class="input-item"
                  />
                  <span class="input-prefix">
                    <base-icon class="input-prefix__icon" icon="mail" />
                  </span>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<style lang="scss">
.authenticate {
  &__header {
    display: flex;
    flex-direction: column;
    align-items: center;
  }
  &__logo {
    filter: drop-shadow(0 4px 4px rgba(0, 0, 0, 0.25));
    @include rem(padding, 8, 0);
  }
  &__title {
    letter-spacing: 0.5px;
    line-height: 150%;
    color: $dark;
    font-size: 1rem;
    @include rem(padding, 8, 0);
  }
  &__desc {
    letter-spacing: 0.5px;
    font-size: 12px;
    line-height: 120%;
  }
}
.input-wrapper {
  position: relative;
  width: 100%;
  display: inline-block;
  .input-item {
    position: relative;
    border: 1px solid #ebf0ff;
    border-radius: 5px;
    width: 100%;
    outline: none;
    height: 3rem;
    font-weight: bold;
    font-size: 12px;
    letter-spacing: 0.5px;
    color: $gray;
    @include rem(padding, 13, 16, 13, 50);
    @include placeholder {
      font-weight: 400;
    }
    &:focus {
      border: 1px solid $input-border-active;
      outline: none;
    }
  }
  .input-prefix {
    position: absolute;
    left: 1rem;
    top: 50%;
    display: flex;
    align-items: center;
    color: rgba(0, 0, 0, 0.65);
    line-height: 0;
    transform: translateY(-50%);
    &__icon {
      color: $gray;
    }
  }
}
</style>
