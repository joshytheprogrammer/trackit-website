<template>
  <div class="faq" :class="{'wide' : !mobile}">
    <div class="_header">
      <h1>Frequently Asked Questions</h1>
    </div>
    <div class="_card" :class="{'wide' : !mobile}" v-for="q in data" :key="q.id">
      <div class="_question">
        <span>{{q.question}}</span>
        <div class="_sign">
          <span title="Close" v-if="ansID == q.id" @click="showAns(null)">C</span>
          <span title="Open" v-else @click="showAns(q.id)">O</span>
        </div>
      </div>
      <div class="_ans" v-if="ansID == q.id">
        <span>{{q.answer}}</span>
      </div>
    </div>
  </div>
</template>

<script>
import {mapGetters} from "vuex"
export default {
  computed: {
    ...mapGetters({
      mobile: 'mobile/mobile',
    })
  },
  data() {
    return {
      data: [
        {
          id: 0,
          question: "What is the MCE program?",
          answer: "Providing the technology skills and certifications students need to succeed. "
        },
        {
          id: 1,
          question: "What are the services we offer?",
          answer: "Interactive Smart Board, Learning Technology Installations, Microsoft Certified Educator, ICT Lab Setting"
        }
      ],
      showingAns: false,
      ansID: null
    }
  },
  methods: {
    showAns(id) {
      this.showingAns  = !this.showingAns
      this.ansID = id
    }
  }
}
</script>

<style lang="scss" scoped>
.faq {
  margin: 1rem;
  display: flex;
  flex-direction: column;
  justify-content: center;

  ._header {
    margin: 0.5rem 0;
  }

  ._card {
    border: 1px solid $dark;
    border-radius: 4px;
    padding: 0.5rem;
    background: $grey;
    width: 100%;
    margin: 1rem 0;

    &.wide {
      width: 50%;
    }

    ._question {
      display: flex;
      justify-content: space-between;

      span {
        font-size: 18px;
        font-weight: 500;
      }

      ._sign {
        cursor: pointer;
        padding: 0.1rem 0.5rem;
        border-radius: 50%;

        &:hover {
          background: $primary;
          color: $light;
        }
      }
    }

    ._ans {
      margin: 0.5rem 0;
      span {
        font-size: 14px;
      }
    }

    
  }
}
</style>