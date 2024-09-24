<template>
    <div class="font-sans text-gray-800 bg-gray-100">
      <!-- Navigation Bar -->
      <nav class="bg-white shadow-md fixed top-0 left-0 right-0 z-10">
        <div class="container mx-auto px-4">
          <div class="flex justify-between items-center h-16">
            <div class="flex items-center">
              <img src="/placeholder.svg" alt="KOPS Logo" class="h-10 w-10 mr-2">
              <span class="font-bold text-xl text-gray-800">株式会社KOPS</span>
            </div>
            <div class="hidden md:flex space-x-4">
              <a href="#service" class="text-gray-600 hover:text-gray-800">サービス概要</a>
              <a href="#flow" class="text-gray-600 hover:text-gray-800">サービスの流れ</a>
              <a href="#achievements" class="text-gray-600 hover:text-gray-800">実績紹介</a>
              <a href="#reviews" class="text-gray-600 hover:text-gray-800">お客様の声</a>
              <a href="#consultant" class="text-gray-600 hover:text-gray-800">DXコンサルタント</a>
              <a href="#contact" class="text-gray-600 hover:text-gray-800">お問い合わせ</a>
            </div>
            <div class="md:hidden">
              <button @click="toggleMenu" class="text-gray-600 hover:text-gray-800 focus:outline-none">
                <svg class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path v-if="!isMenuOpen" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
                  <path v-else stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
                </svg>
              </button>
            </div>
          </div>
        </div>
        <!-- Mobile menu -->
        <div v-if="isMenuOpen" class="md:hidden">
          <div class="px-2 pt-2 pb-3 space-y-1 sm:px-3">
            <a href="#service" class="block px-3 py-2 text-gray-600 hover:text-gray-800">サービス概要</a>
            <a href="#flow" class="block px-3 py-2 text-gray-600 hover:text-gray-800">サービスの流れ</a>
            <a href="#achievements" class="block px-3 py-2 text-gray-600 hover:text-gray-800">実績紹介</a>
            <a href="#reviews" class="block px-3 py-2 text-gray-600 hover:text-gray-800">お客様の声</a>
            <a href="#consultant" class="block px-3 py-2 text-gray-600 hover:text-gray-800">DXコンサルタント</a>
            <a href="#contact" class="block px-3 py-2 text-gray-600 hover:text-gray-800">お問い合わせ</a>
          </div>
        </div>
      </nav>
  
      <!-- Header -->
      <header class="bg-gradient-to-r from-green-400 to-blue-500 text-white py-24 px-4 mt-16">
        <div class="container mx-auto text-center">
          <h1 class="text-4xl font-bold mb-4">中小企業のデジタル化を、手軽に、スピーディに。<br>月額29,800円でDXを実現！</h1>
          <p class="text-xl mb-8">業務効率化とコスト削減をサポート。無料相談はこちらから！</p>
          <a href="#contact" class="bg-green-500 hover:bg-green-600 text-white font-bold py-3 px-6 rounded-full text-lg transition duration-300 ease-in-out transform hover:scale-105">
            今すぐ無料相談を申し込む
          </a>
          <p class="mt-4 text-lg font-semibold">先着5名様は初月無料！</p>
        </div>
      </header>
  
      <!-- Service Overview -->
      <section id="service" class="py-16 px-4">
        <div class="container mx-auto">
          <h2 class="text-3xl font-bold mb-8 text-center">DXコンサルティングで、貴社の成長を加速</h2>
          <p class="text-lg mb-8 text-center max-w-3xl mx-auto">
            株式会社KOPSは、不動産業、建設業、清掃業などの小規模事業者を対象に、デジタル化を通じた業務効率化とコスト削減をサポートします。大規模プロジェクトで培ったノウハウを、月額29,800円で、小規模企業でも実現可能な形でご提案します。
          </p>
          <div class="grid md:grid-cols-3 gap-8 mb-12">
            <div class="bg-white p-6 rounded-lg shadow-md">
              <h3 class="text-xl font-semibold mb-4">低価格</h3>
              <p>月額29,800円のリーズナブルな価格設定</p>
            </div>
            <div class="bg-white p-6 rounded-lg shadow-md">
              <h3 class="text-xl font-semibold mb-4">即レスポンス</h3>
              <p>迅速な対応でお客様の問題を即座に解決</p>
            </div>
            <div class="bg-white p-6 rounded-lg shadow-md">
              <h3 class="text-xl font-semibold mb-4">幅広い業務対応</h3>
              <p>ウェブサイト制作、業務効率化支援、ITシステム導入代行など、さまざまなサービスを提供</p>
            </div>
          </div>
          <div class="text-center">
            <a href="#contact" class="bg-green-500 hover:bg-green-600 text-white font-bold py-3 px-6 rounded-full text-lg transition duration-300 ease-in-out transform hover:scale-105">
              今すぐ無料相談
            </a>
          </div>
        </div>
      </section>
  
      <!-- Service Flow -->
      <section id="flow" class="bg-gray-200 py-16 px-4">
        <div class="container mx-auto">
          <h2 class="text-3xl font-bold mb-12 text-center">サービスの流れ</h2>
          <div class="grid md:grid-cols-4 gap-8">
            <div class="bg-white p-6 rounded-lg shadow-md">
              <h3 class="text-xl font-semibold mb-4">1. 現状分析と課題ヒアリング</h3>
              <p>業務内容や課題を詳細にヒアリングし、現在の業務状況を分析します。</p>
            </div>
            <div class="bg-white p-6 rounded-lg shadow-md">
              <h3 class="text-xl font-semibold mb-4">2. 最適な提案</h3>
              <p>あなたの企業に最適なデジタル化の方法を提案します。お客様が気づいていない課題も浮き彫りにします。</p>
            </div>
            <div class="bg-white p-6 rounded-lg shadow-md">
              <h3 class="text-xl font-semibold mb-4">3. 実行支援</h3>
              <p>提案内容を実行し、システム導入や業務の改善を支援します。</p>
            </div>
            <div class="bg-white p-6 rounded-lg shadow-md">
              <h3 class="text-xl font-semibold mb-4">4. 継続的なサポート</h3>
              <p>実行後もサポートを継続し、必要に応じてさらなる改善を行います。</p>
            </div>
          </div>
          <div class="text-center mt-12">
            <a href="#contact" class="bg-green-500 hover:bg-green-600 text-white font-bold py-3 px-6 rounded-full text-lg transition duration-300 ease-in-out transform hover:scale-105">
              無料相談はこちら
            </a>
          </div>
        </div>
      </section>
  
      <!-- Achievements -->
      <section id="achievements" class="py-16 px-4">
        <div class="container mx-auto">
          <h2 class="text-3xl font-bold mb-12 text-center">実績紹介</h2>
          <div class="grid md:grid-cols-2 gap-8 mb-12">
            <div class="bg-white p-6 rounded-lg shadow-md">
              <h3 class="text-xl font-semibold mb-4">GASを活用した業務自動化</h3>
              <p>メール提案活動の自動化を実現。作業時間を1/3に削減した実績。</p>
            </div>
            <div class="bg-white p-6 rounded-lg shadow-md">
              <h3 class="text-xl font-semibold mb-4">ウェブサイトリニューアル</h3>
              <p>SEO強化で問い合わせ数が倍増した事例。</p>
            </div>
          </div>
          <div class="text-center">
            <a href="#contact" class="bg-green-500 hover:bg-green-600 text-white font-bold py-3 px-6 rounded-full text-lg transition duration-300 ease-in-out transform hover:scale-105">
              今すぐ無料相談
            </a>
          </div>
        </div>
      </section>
  
      <!-- Customer Reviews -->
      <section id="reviews" class="bg-gray-200 py-16 px-4">
        <div class="container mx-auto">
          <h2 class="text-3xl font-bold mb-12 text-center">お客様の声</h2>
          <div class="grid md:grid-cols-2 gap-8 mb-12">
            <div class="bg-white p-6 rounded-lg shadow-md">
              <p class="mb-4">「丁寧なヒアリングで、私たちが気づいていなかった課題を発見し、最適な解決策を提案してもらいました。」</p>
              <p class="font-semibold">- A社 代表取締役</p>
            </div>
            <div class="bg-white p-6 rounded-lg shadow-md">
              <p class="mb-4">「DX導入後、業務効率が飛躍的に向上し
  
  ました。サポートがとても迅速で助かっています。」</p>
              <p class="font-semibold">- B社 経営企画部長</p>
            </div>
          </div>
          <div class="text-center">
            <a href="#contact" class="bg-green-500 hover:bg-green-600 text-white font-bold py-3 px-6 rounded-full text-lg transition duration-300 ease-in-out transform hover:scale-105">
              今すぐ無料相談
            </a>
          </div>
        </div>
      </section>
  
      <!-- Consultant Introduction -->
      <section id="consultant" class="py-16 px-4">
        <div class="container mx-auto">
          <h2 class="text-3xl font-bold mb-12 text-center">あなたのDX顧問 - 馬込 浩</h2>
          <div class="flex flex-col md:flex-row items-center justify-center">
            <img src="/placeholder.svg" alt="馬込 浩" class="rounded-full w-64 h-64 object-cover mb-8 md:mb-0 md:mr-12" />
            <div class="max-w-lg">
              <p class="text-lg mb-8">
                大規模プロジェクトから小規模な案件まで、幅広く対応できる経験豊富なDXコンサルタントです。ITシステムの導入や業務効率化の実績を多数持ち、どのような課題にも迅速に対応いたします。
              </p>
              <a href="#contact" class="bg-green-500 hover:bg-green-600 text-white font-bold py-3 px-6 rounded-full text-lg transition duration-300 ease-in-out transform hover:scale-105">
                今すぐ無料相談
              </a>
            </div>
          </div>
        </div>
      </section>
  
      <!-- Contact Form -->
      <section id="contact" class="bg-gray-200 py-16 px-4">
        <div class="container mx-auto">
          <h2 class="text-3xl font-bold mb-12 text-center">今すぐ無料相談をお申し込みください</h2>
          <div class="max-w-3xl mx-auto bg-white rounded-lg shadow-md overflow-hidden">
            <iframe 
              src="https://docs.google.com/forms/d/e/1FAIpQLSd2NzTik0b26K6Cwtx0yIyqllwwKxfiedZx7fOb7fervW-9Fg/viewform?embedded=true" 
              width="100%" 
              height="1260" 
              frameborder="0" 
              marginheight="0" 
              marginwidth="0"
              title="無料相談申し込みフォーム"
            >
              読み込んでいます…
            </iframe>
          </div>
        </div>
      </section>
  
      <!-- FAQ -->
      <section class="py-16 px-4">
        <div class="container mx-auto">
          <h2 class="text-3xl font-bold mb-12 text-center">よくある質問</h2>
          <div class="max-w-3xl mx-auto">
            <div class="mb-8">
              <h3 class="text-xl font-semibold mb-2">DXって何ですか？</h3>
              <p>DXとはデジタルトランスフォーメーションの略で、デジタル技術を活用して業務効率を上げ、新たなビジネス価値を創造する取り組みです。</p>
            </div>
            <div class="mb-8">
              <h3 class="text-xl font-semibold mb-2">どのような企業が対象ですか？</h3>
              <p>主に1～20名規模の不動産業、建設業、清掃業など、業務効率化やデジタル化を考えている企業様が対象です。</p>
            </div>
          </div>
          <div class="text-center mt-12">
            <a href="#contact" class="bg-green-500 hover:bg-green-600 text-white font-bold py-3 px-6 rounded-full text-lg transition duration-300 ease-in-out transform hover:scale-105">
              今すぐ無料相談
            </a>
          </div>
        </div>
      </section>
  
      <!-- Footer -->
      <footer class="bg-gray-800 text-white py-8 px-4">
        <div class="container mx-auto">
          <div class="grid md:grid-cols-2 gap-8">
            <div>
              <h3 class="text-xl font-semibold mb-4">株式会社KOPS</h3>
              <p>住所: 千葉県船橋市前原西2-14-2 津田沼駅前安田ビル別館2階26</p>
              <p>電話番号: 080-9643-5493</p>
              <p>メールアドレス: h-magome@ko-partners.biz</p>
            </div>
            <div class="text-right">
              <p>&copy; 2024 株式会社KOPS All Rights Reserved.</p>
            </div>
          </div>
        </div>
      </footer>
    </div>
  </template>
  
  <script setup>
import { ref, onMounted, onBeforeUnmount } from 'vue'

const isMenuOpen = ref(false)

const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value
}

onMounted(() => {
  const resizeIframe = () => {
    const iframe = document.querySelector('iframe')
    if (iframe) {
      iframe.style.height = window.innerWidth < 640 ? '1400px' : '1260px'
    }
  }

  window.addEventListener('resize', resizeIframe)
  resizeIframe()

  // コンポーネントがアンマウントされる前にイベントリスナーを削除
  onBeforeUnmount(() => {
    window.removeEventListener('resize', resizeIframe)
  })
})
</script>
  
  <style scoped>
  @media (max-width: 640px) {
    #contact iframe {
      width: 100%;
    }
  }
  </style>