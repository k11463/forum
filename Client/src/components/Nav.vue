<template>
    <div class="bg">
        <div class="left center">
            <h2>
                實 驗 室 論 壇
            </h2>
        </div>
        <div class="mid">
            <div class="selection">
                <div class="select">
                    <button class="selected center">
                        {{ selections[selection] }}
                    </button>
                    <ul>
                        <li v-for="(select, id) in  selections" :key="id" class="center" @click="ChangeSelection(id)">
                            {{ select }}
                        </li>
                    </ul>
                </div>
            </div>
            <div class="searchBox center">
                <input type="text" size=10>
            </div>
            <div class="send">
                <button>
                    搜 尋
                </button>
            </div>
        </div>
        <div class="right">
            <div class="box" v-for="rc in RightCols" :key="rc">
                {{ rc }}
                <div class="botLine"></div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            selections: [
                "找 標 題", "找 作 者", "找 內 容"
            ],
            selection: 0,
            isLogin: false,
            RightCols: [
                "註 冊", "登 入"
            ]
        }
    },
    methods: {
        ChangeSelection(val) {
            this.selection = val;
        }
    }
}
</script>


<style lang="scss">
$BorderColor:rgb(110, 95, 53);
.bg {
    background-color: #dfb669;
    width: 100vw;
    height: 6vh;
    font-family: "標楷體";
    .left {
        width: 20%;
        height: 100%;
        font-weight: bold;
        float: left;
        h2 {
            cursor: pointer;
        }
    }
    .mid {
        width: 60%;
        height: 100%;
        float: left;
        .selection {
            width: 15%;
            height: 100%;
            float: left;
            user-select: none;
            .select {
                height: 100%;
                position: relative;
                display: flex;
                justify-content: flex-end;
                align-items: center;
                .selected {
                    width: 72px;
                    height: 28px;
                    background-color: #fff;
                    border: 1px solid $BorderColor;
                    border-radius: 5px 0 0 5px;
                    font-weight: bold;
                    color: rgb(194, 167, 59);
                }
                .selected:focus + ul {
                    opacity: 1;
                    transform: translateY(8px);
                }
                .selected:hover {
                    background-color: rgb(255, 241, 203);
                }
                ul {
                    opacity: 0;
                    padding: 0;
                    top: 48px;
                    left: 0;
                    width: 100px;
                    height: 84px;
                    position: absolute;
                    list-style: none;
                    border-radius:  5px 5px 5px 5px;
                    transform: translateY(-8px);
                    transition: 0.8s;
                    li {
                        font-weight: bold;
                        color: rgb(194, 167, 59);
                        width: 100%;
                        height: 28px;
                        background-color: #fff;
                    }
                    li:hover {
                        background-color: rgb(255, 241, 203);
                    }
                    li:first-child {
                        border-radius: 5px 5px 0 0;
                    }
                    li:last-child {
                        border-radius: 0 0 5px 5px;
                    }
                }
            }
        }
        .searchBox {
            width: 70%;
            height: 100%;
            float: left;
            input {
                width: 100%;
                height: 28px;
                background-color: #fff;
                border-top: 1px solid $BorderColor;
                border-right: 1px solid $BorderColor;
                border-bottom: 1px solid $BorderColor;
                font-weight: bold;
                color: rgb(110, 85, 15);
                padding-left: 4px;
            }
            input:focus {
                background-color: rgb(230, 224, 208);
            }
        }
        .send {
            width: 15%;
            height: 100%;
            float: left;
            display: flex;
            align-items: center;
            justify-content: flex-start;
            button {
                width: 52px;
                height: 28px;
                border-top: 1px solid $BorderColor;
                border-right: 1px solid $BorderColor;
                border-bottom: 1px solid $BorderColor;
                border-radius: 0 5px 5px 0;
                background-color: rgb(190, 147, 66);
                color: rgb(255, 249, 240);
                font-weight: bold;
                transform: translateY(-4px);
                box-shadow: 2px 4px 2px 1px rgba(0, 0, 0, 0.4);
            }
            button:active {
                box-shadow: 0 0 0 0;
                transform: translateY(0.2px);
            }
        }
    }
    .right {
        width: 20%;
        height: 100%;
        float: left;
        display: flex;
        justify-content: space-around;
        align-items: center;
        .box {
            height: 32px;
            font-size: 16px;
            font-weight: bold;
            float: right;
            display: flex;
            align-items: center;
            cursor: pointer;
            color: rgb(110, 85, 15);
            position: relative;
            .botLine {
                margin-top: 16px;
                width: 44px;
                position: absolute;
                border-bottom: 2px solid rgb(110, 85, 15);
                transition: 0.4s;
                opacity: 0;
                transform: translateY(4px);
            }
        }
        .box:hover > .botLine {
            opacity: 1;
            transform: translateY(-2px);
        }
    }
}
.center {
    display: flex;
    justify-content: center;
    align-items: center;
}
</style>

