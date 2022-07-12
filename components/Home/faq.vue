<template>
  <div class="faq" :class="{'wide' : !mobile}" id="faq">
    <div class="_header">
      <h2>Frequently Asked Questions</h2>
    </div>
    <div class="content">
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
          question: "What are the services you offer?",
          answer: "We offer all the services described above, you can also visit the quotation page to find out more about your specific page, or contact us via the contact page."
        },
        {
          id: 1,
          question: "Does the MCE cost money?",
          answer: "Yes it does, you can click the 'Get A Quote' button above to receive a price quote."
        },
        {
          id: 2,
          question: "What happens after the completion of the program -MCE?",
          answer: "You will be granted a certificate issued by our partners, Microsoft."
        },
        {
          id: 3,
          question: "How much does it cost to install the Interactive Smart Board and how long would it take to install?",
          answer: "The board can cost anywhere from 900k - 5M and take anywhere from a week to 6 months to Install. 'Get a Quote' to find out more about your specific use case."
        },
        {
          id: 4,
          question: "What knowledge/skills do I need to have to undergo the MCE program and other programs you offer?",
          answer: "No knowledge is required, but a basic knowledge of computers is recommended. We provide computers as well as internet access all through your time with us.",
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
  align-items: center;
  justify-content: center;
  text-align: center;

  ._header {
    margin: 0.5rem 0;

    h2 {
      font-weight: 400;
      font-size: 36px;
    }
  }

  .content {
    ._card {
      border: 1px solid $dark;
      border-radius: 4px;
      padding: 0.5rem;
      background: $grey;
     
      margin: 1rem 0;

      ._question {
        display: flex;
        justify-content: space-between;
        

        span {
          font-size: 16px;
          font-weight: 400;
          text-align: center;
        }

        ._sign {
          cursor: pointer;
          padding: 0.1rem 0.5rem;
          border-radius: 50%;
          width: fit-content;
          height: fit-content;

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
}
</style>