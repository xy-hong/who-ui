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

<div id="main-box">
    <div id="chart-box">
        {#each records as record}
        <div>{record.time} {record.nick}: {record.message}</div>
        {/each}
    </div>
    <div>
        <textarea />
    </div>
</div>

<style>
    #main-box {
        max-width: 600px;
        margin: 0 auto;
    }

    #chart-box {
        width: 100%;
        background-color: #20201d;
        color: #a6a28c;
        border: 1px solid #4f4d42;
    }

    
</style>

