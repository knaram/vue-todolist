<template>
    <div class="add">
        <input
        v-model="newItem"
        type="text"
        class="add__list"
        placeholder="Enter your task here"
        />
        <button class="add__button">add list</button>
    </div>
</template>

<script>
export default {};
</script>

<style scoped lang="scss">
$point-color: #77b4be;

.add {
    position: relative;
    width: 100%;
    height: 46px;
    border-radius: 25px;
    overflow: hidden;
    box-shadow: 2px 2px 4px $point-color;

    &__list {
        border: 0;
        width: 100%;
        height: 100%;
        padding: 0 5%;
        background-color: #97cdd7;
        color: #fff;
        font-size: 0.9rem;

        &:focus {
        outline: none;
        }

        &::placeholder {
        color: #d5e8eb;
        }
    }

    &__button {
        position: absolute;
        top: 50%;
        right: 1.5%;
        width: 36px;
        height: 36px;
        margin-top: -18px;
        font-size: 0;
        border-radius: 18px;
        background-color: rgba(255, 255, 255, 0.7);

        &:before {
        content: "";
        position: absolute;
        left: 50%;
        top: 50%;
        margin: -15% 0 0 -1px;
        width: 2px;
        height: 30%;
        background-color: $point-color;
        }

        &:after {
        content: "";
        position: absolute;
        left: 50%;
        top: 50%;
        margin: -1px 0 0 -15%;
        width: 30%;
        height: 2px;
        background-color: $point-color;
        }
    }
}
</style>