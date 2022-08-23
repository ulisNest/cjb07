<script>
  // your script goes here
  import { io } from 'socket.io-client';
  const socket = io();
  
  let receivedMessages = [];
  socket.on('logMsg', (data) => {
    console.log("added msg");
    console.log("lista: ", receivedMessages);
    receivedMessages = [...receivedMessages, data.msg];
  });

</script>

<section class="logWindow">
  {#each receivedMessages as msg}
     <span>{msg}</span>
  {/each}
</section>

<style>
    section.logWindow {
      display: flex;
      flex-direction: column;
      padding: 0.5%;
      outline: 1px solid gray;
      height: 65vh;
      border-radius: 0.5%;
      margin-bottom: 1%;
      text-align: left;
      overflow: auto;
    }
</style>
