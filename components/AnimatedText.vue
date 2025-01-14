<template>
    <div class="typing-container">
        <span class="typing-text">{{ currentText }}</span>
        <span class="cursor"></span>
    </div>
</template>

<script setup>
import { ref, onMounted } from 'vue';

const words = ref(['Frontend', 'Backend', 'Game', 'Graphic']);
const currentText = ref('');
const typingSpeed = 150;
const erasingSpeed = 100;
const newWordDelay = 2000;

let wordIndex = 0;
let charIndex = 0;
let isTyping = true;

const type = () => {
    if (wordIndex >= words.value.length) {
        wordIndex = 0;
    }

    const currentWord = words.value[wordIndex];

    if (isTyping) {
        currentText.value = currentWord.substring(0, charIndex + 1);
        charIndex++;

        if (charIndex === currentWord.length) {
            isTyping = false;
            setTimeout(type, newWordDelay);
        } else {
            setTimeout(type, typingSpeed);
        }
    } else {
        currentText.value = currentWord.substring(0, charIndex - 1);
        charIndex--;

        if (charIndex === 0) {
            isTyping = true;
            wordIndex++;
            setTimeout(type, typingSpeed);
        } else {
            setTimeout(type, erasingSpeed);
        }
    }
};

onMounted(() => {
    type();
});
</script>

<style scoped>
.typing-container {
    display: inline-block;
}

.typing-text {
    color: var(--blue);
}

.cursor {
    display: inline-flex;
    align-items: center;
    width: 6px;
    height: 48px;
    background: black;
    margin-left: 16px;
    margin-bottom: -4px;
    animation: blink 0.7s infinite;
}

@keyframes blink {

    0%,
    100% {
        opacity: .6;
    }

    50% {
        opacity: 0;
    }
}
</style>