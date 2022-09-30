<template>
  <div class="event-card">
    <span>Description : {{ auction.description }} </span>
    <h5>Type: {{ auction.type }}</h5>
    <h5>
      Successful Bid : {{ auction.successfulBid.id }} Amount :{{
        auction.successfulBid.amount
      }}
    </h5>
  </div>
</template>
<script>
export default {
  name: 'EventCard',
  props: {
    auction: {
      type: Object,
      required: true
    }
  }
}
</script>
<style scoped>
.event-card {
  padding: 20px;
  width: 250px;
  cursor: pointer;
  background: white;
  border: 1px solid #ffe600;
  margin-bottom: 18px;
  transition: 0.25s;
  border-radius: 20px;
}

.event-card:hover {
  background: transparent;
  color: white;
  transform: scale(1.01);
  border-radius: 20px;
  box-shadow: 0 3px 12px 0 rgba(236, 202, 5, 0.753);
}

.event-link {
  color: #2c3e50;
  text-decoration: none;
}
</style>
