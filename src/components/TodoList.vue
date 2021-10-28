<template>
    <div class="list__area">
        <p class="message">YOU'VE GOT <em>3</em> TASKS TODAY</p>
        <ul class="list">
            <li class="list__item">
                <input
                    class="list__checkbox"
                    type="checkbox"
                    name="list-item"
                    id="list-item-01"
                />
                <label for="list-item-01">
                    UI/UX 회의<span class="date">10.28</span>
                </label>
                <button class="list__del">delete</button>
            </li>

            <li class="list__item">
                <input
                    class="list__checkbox"
                    type="checkbox"
                    name="list-item"
                    id="list-item-02"
                />
                <label for="list-item-02">
                    마켓컬리 장보기<span class="date">10.28</span>
                </label>
                <button class="list__del">delete</button>
            </li>

            <li class="list__item">
                <input
                    class="list__checkbox"
                    type="checkbox"
                    name="list-item"
                    id="list-item-03"
                />
                <label for="list-item-03">
                    얌이 화장실 사기<span class="date">10.28</span>
                </label>
                <button class="list__del">delete</button>
            </li>
        </ul>
    </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
$point-color: #fff;
$list-height: 52px;

.list__area {
    padding-top: 10%;

    .message {
        color: #eee;
        font-size: 0.8rem;
        font-weight: bold;
        text-align: right;
        letter-spacing: 0.15rem;

        em {
        color: #fff;
        font-size: 1.5rem;
        }
    }
}

.list {
    padding-top: 5%;

    &__item {
        display: flex;
        align-items: center;
        background-color: $point-color;
        height: $list-height;
        padding: 0 5%;
        border-radius: 6px;
        box-shadow: -4px 4px 5px #6eb5c2;

        .list__checkbox {
        width: 0;
        height: 0;
        }

        label {
        position: relative;
        width: calc(100% - 40px);
        height: 100%;
        line-height: $list-height;
        padding-left: 24px;
        font-size: 0.9rem;

        &:before {
            content: "";
            position: absolute;
            left: 0;
            top: 50%;
            margin-top: -6px;
            display: inline-block;
            width: 12px;
            height: 12px;
            border: 1px solid #777;
            border-radius: 3px;
            transition: border-radius 0.5s;
        }

        .date {
            font-size: 0.75rem;
            color: #888;
            padding-left: 5px;
        }
        }

        .list__checkbox:checked + label {
        color: #999;
        text-decoration: line-through;

        &:before {
            background-color: #6eb5c2;
            border-color: #6eb5c2;
            border-radius: 10px;
        }
        }

        .list__del {
        position: relative;
        font-size: 0;
        width: 30px;
        height: 30px;

        &:before {
            content: " ";
            position: absolute;
            left: 40%;
            top: 44%;
            width: 12px;
            border-top: 1px solid #666;
            transform: rotate(45deg);
        }

        &:after {
            content: " ";
            position: absolute;
            left: 40%;
            top: 44%;
            width: 12px;
            border-top: 1px solid #666;
            transform: rotate(-45deg);
        }
        }
    }

    &__item + &__item {
        margin-top: 10px;
    }
}
</style>