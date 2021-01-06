<script lang="ts">
    // let nick = prompt('输入你的昵称:')
    let nick = 'hxy'
    let records = [
        { nick: 'hxy', message: '你好(*´▽｀)ノノ', time: '22:50'},
        { nick: 'zhh', message: '(*´▽｀)ノノ哟哟哟', time: '22:56'},
        { nick: 'zhh', message: '你从哪来来', time: '22:58'},
        { nick: 'hxy', message: '新世界来的', time: '22:59'},
    ]
</script>

<div id="chart-container">
    <div>
        <div id="chart-box">
            {#each records as record}
            <div>{record.time} {record.nick}: {record.message}</div>
            {/each}
        </div>
        <div>
            <input />
            <button>SEND</button>
        </div>
    </div>
</div>

<style>
    #chart-container {
        display: flex;
        justify-content: center;
    }

    #chart-box {
        background-color: whitesmoke;
        border: 1px solid gray;
    }
</style>

