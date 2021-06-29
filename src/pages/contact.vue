<template>
  <Layout>
    <h1 class="title">Say hi!</h1>
    <p class="note">Leave me a note with any questions you might have, I'll get back to you as soon as possible.</p>

    <form>

      <div class="group">
        <div style="flex: 1;margin-right: 10px;">
          <label class="label">Your name</label>
          <input type="text" class="input"/>
        </div>

        <div style="flex: 1">
          <label class="label">Your email</label>
          <input type="email" class="input"/>
        </div>
      </div>


      <div>
        <label class="label">Message</label>
        <textarea class="input textarea"/>
      </div>

      <div>
        <input class="submit" type="submit" value="Submit form"/>
      </div>

      
    </form>

  </Layout>
</template>

<script>
import Index from './Index.vue'
export default {
  components: { Index },
  metaInfo: {
    title: 'Say hi'
  }
}
</script>

<style>

  .title {
    font-size: 4rem;
    margin: 0 0 4rem
  }

  .note {
    font-size: 1.15rem;
    line-height: 1.5;
    margin-bottom: 4rem;
  }

  .group {
    display: flex;
    justify-content: space-between;
    margin-bottom: 1rem;
  }

  .label {
    display: block;
    font-weight: 700;
    margin-bottom: .5rem;
  }

  .input {
    background: transparent;
    border: 1px solid #f3f3f3;
    outline: none;
    border-radius: .3rem;
    padding: .8rem 1rem;
    color: inherit;
    font-size: 1rem;
    width: 100%;
    box-sizing: border-box;
  }

  .textarea {
    resize: none;
    height: 140px;
  }

  .submit {
    color: #ffffff;
    padding: .8rem 1.6rem;
    outline: none;
    border: 0;
    border-radius: .3rem;
    background-color: #000000;
    font-size: .8rem;
    margin-top: 2rem;
  }

</style>
