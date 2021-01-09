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

<div class="container">
    <div class="main">
        <div class="status-bar">状态栏,玩家准备就绪</div>
        {#each records as record}
        <div class="message">
            <span class="nick">
                <span>{ record.nick }</span>
            </span>
            <span class="message-detail">{ record.message }</span>
        </div> 
        {/each}
    </div>
    <div class="footer">
        <div class="input-box">
            <textarea autofocus></textarea>
        </div>
    </div>
</div>   

<style>
* {
    box-sizing: border-box;
    background-color: #212121;
    color: #e0e0e0;
    font-family: 'DejaVu Sans Mono', monospace;
    font-size: 12px;
    margin: 0;
}

.status-bar {
    padding: 1em;
    color: #99c210;
}

.main {
    margin: 0 auto;
    max-width: 600px;
    margin-bottom: 50px;
}

.footer {
    position: fixed;
    bottom: 0;
    left: 0;
    width: 100%;
}

.footer .input-box {
    max-width: 600px;
    margin: 0 auto;
}

.footer .input-box textarea {
    width: 100%;
    min-height: 50px;
    border-right: none;
    border-bottom: none;
    resize: none;
}

.footer .input-box textarea:focus {
    outline: none;
}

.message {
    border-left: 1px solid #535353;
    padding-bottom: 1em;
    margin: 0;
}

.nick {
    float: left;
    width: 16em;
    margin-left: -17em;
    text-align: right;
    white-space: nowrap;
}

@media screen and (max-width: 600px){
    .nick {
        float: none;
        width: auto;
        margin: 0;
        padding-left: 2px;
        display: block;
        text-align: left;
    }

    .footer {
        left: 8px;
    }
}

.nick span {
    color: #9568aa;
}

.message .message-detail {
    margin-left: 1em;
}

</style>

