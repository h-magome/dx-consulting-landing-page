<template>
    <div class="font-sans text-gray-800 bg-gray-100">
      <!-- Navigation Bar -->
      <nav class="bg-white shadow-md fixed top-0 left-0 right-0 z-10">
        <div class="container mx-auto px-4">
          <div class="flex justify-between items-center h-16">
            <div class="flex items-center cursor-pointer" @click="scrollToTop">
              <img src="/images/KOPSロゴ.png" alt="KOPS Logo" class="h-16 w-16 mr-2">
              <span class="font-bold text-xl text-green-600">あなたのDX顧問</span>
            </div>
            <div class="hidden md:flex items-center space-x-6">
              <a href="#service" class="text-gray-700 hover:text-green-500 font-medium transition duration-300 ease-in-out border-b-2 border-transparent hover:border-green-500" @click.prevent="scrollToElement('#service')">サービス概要</a>
              <a href="#flow" class="text-gray-700 hover:text-green-500 font-medium transition duration-300 ease-in-out border-b-2 border-transparent hover:border-green-500" @click.prevent="scrollToElement('#flow')">サービスの流れ</a>
              <a href="#achievements" class="text-gray-700 hover:text-green-500 font-medium transition duration-300 ease-in-out border-b-2 border-transparent hover:border-green-500" @click.prevent="scrollToElement('#achievements')">実績紹介</a>
              <a href="#reviews" class="text-gray-700 hover:text-green-500 font-medium transition duration-300 ease-in-out border-b-2 border-transparent hover:border-green-500" @click.prevent="scrollToElement('#reviews')">お客様の声</a>
              <a href="#consultant" class="text-gray-700 hover:text-green-500 font-medium transition duration-300 ease-in-out border-b-2 border-transparent hover:border-green-500" @click.prevent="scrollToElement('#consultant')">DXコンサルタント</a>
              <a href="#contact" class="bg-green-500 text-white hover:bg-green-600 font-bold py-2 px-4 rounded-full transition duration-300 ease-in-out transform hover:scale-105" @click.prevent="scrollToElement('#contact')">お問い合わせ</a>
            </div>
            <div class="md:hidden">
              <button @click="toggleMenu" class="text-gray-600 hover:text-green-500 focus:outline-none">
                <svg class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path v-if="!isMenuOpen" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
                  <path v-else stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
                </svg>
              </button>
            </div>
          </div>
        </div>
        <!-- Mobile menu -->
        <div v-if="isMenuOpen" class="md:hidden bg-white shadow-lg">
          <div class="px-2 pt-2 pb-3 space-y-1 sm:px-3">
            <a href="#service" class="block px-3 py-2 text-gray-700 hover:text-green-500 hover:bg-gray-100 rounded-md transition duration-300 ease-in-out">サービス概要</a>
            <a href="#flow" class="block px-3 py-2 text-gray-700 hover:text-green-500 hover:bg-gray-100 rounded-md transition duration-300 ease-in-out">サービスの流れ</a>
            <a href="#achievements" class="block px-3 py-2 text-gray-700 hover:text-green-500 hover:bg-gray-100 rounded-md transition duration-300 ease-in-out">実績紹介</a>
            <a href="#reviews" class="block px-3 py-2 text-gray-700 hover:text-green-500 hover:bg-gray-100 rounded-md transition duration-300 ease-in-out">お客様の声</a>
            <a href="#consultant" class="block px-3 py-2 text-gray-700 hover:text-green-500 hover:bg-gray-100 rounded-md transition duration-300 ease-in-out">DXコンサルタント</a>
            <a href="#contact" class="block px-3 py-2 bg-green-500 text-white hover:bg-green-600 rounded-md transition duration-300 ease-in-out">お問い合わせ</a>
          </div>
        </div>
      </nav>
  
      <!-- Header -->
      <header class="bg-gradient-to-r from-green-400 to-blue-500 text-white py-24 px-4 mt-16">
        <div class="container mx-auto text-center">
          <h1 class="text-4xl font-bold mb-4">中小企業のデジタル化を、手軽に、スピーディに。<br>月額29,800円でDXを実現！</h1>
          <p class="text-xl mb-8">業務効率化とコスト削減をサポート。無料相談はこちらから！</p>
          <a href="#contact" class="bg-green-500 hover:bg-green-600 text-white font-bold py-3 px-6 rounded-full text-lg transition duration-300 ease-in-out transform hover:scale-105" @click.prevent="scrollToElement('#contact')">
            今すぐ無料相談を申し込む
          </a>
          <p class="mt-4 text-lg font-semibold">先着5名様は初月無料！</p>
        </div>
      </header>
  
      <!-- DX Support -->
      <section id="dx-support" class="bg-white py-16 px-4">
        <div class="container mx-auto">
          <h2 class="text-3xl font-bold mb-8 text-center text-green-500">様々な背景・ケースでDXを支援</h2>
          <div class="grid md:grid-cols-2 gap-8 mb-12">
            <div class="bg-gray-100 p-6 rounded-lg shadow-md transform hover:scale-105 transition-all duration-300">
              <img src="/images/見積書作成の自動化.svg" alt="見積書作成の自動化" class="h-12 w-12 mb-4 mx-auto">
              <h3 class="text-xl font-semibold mb-4 text-red-500">見積書作成の自動化</h3>
              <div class="flex flex-col md:flex-row justify-between items-center mb-4">
                <div class="bg-red-100 p-4 rounded-lg mb-4 md:mb-0 md:mr-4 flex-1">
                  <h4 class="font-semibold text-red-700 mb-2">現状</h4>
                  <p>見積書の作成が手作業で行われており、時間がかかり、ミスが発生しやすい。</p>
                </div>
                <div class="bg-green-100 p-4 rounded-lg flex-1">
                  <h4 class="font-semibold text-green-700 mb-2">解決策</h4>
                  <p>見積もりシステムを導入し、材料費、労務費などを自動で計算し、テンプレートを使って見積書を生成。過去のデータを蓄積し、参考にすることで見積もりのスピードと正確性が向上します。</p>
                </div>
              </div>
              <div class="bg-blue-100 p-4 rounded-lg">
                <h4 class="font-semibold text-blue-700 mb-2">効果</h4>
                <p>見積作業が大幅に短縮され、ミスの削減と迅速な見積もり提出が可能。</p>
              </div>
            </div>
            
            <div class="bg-gray-100 p-6 rounded-lg shadow-md transform hover:scale-105 transition-all duration-300">
              <img src="/images/プロジェクト進行のデジタル管理.svg" alt="プロジェクト進行のデジタル管理" class="h-12 w-12 mb-4 mx-auto">
              <h3 class="text-xl font-semibold mb-4 text-red-500">プロジェクト進行のデジタル管理</h3>
              <div class="flex flex-col md:flex-row justify-between items-center mb-4">
                <div class="bg-red-100 p-4 rounded-lg mb-4 md:mb-0 md:mr-4 flex-1">
                  <h4 class="font-semibold text-red-700 mb-2">現状</h4>
                  <p>プロジェクトの進行管理が手作業やエクセルで行われており、リアルタイムの進捗確認が難しい。</p>
                </div>
                <div class="bg-green-100 p-4 rounded-lg flex-1">
                  <h4 class="font-semibold text-green-700 mb-2">解決策</h4>
                  <p>プロジェクト管理ツールを導入し、各プロジェクトの進行状況をリアルタイムで確認できるようにする。各現場からの進捗報告もオンラインで行える。</p>
                </div>
              </div>
              <div class="bg-blue-100 p-4 rounded-lg">
                <h4 class="font-semibold text-blue-700 mb-2">効果</h4>
                <p>プロジェクトの進行状況を管理者が即座に確認でき、遅延や問題が早期に発見・対処可能になる。</p>
              </div>
            </div>
            
            <div class="bg-gray-100 p-6 rounded-lg shadow-md transform hover:scale-105 transition-all duration-300">
              <img src="/images/請求書発行の自動化.svg" alt="請求書発行の自動化" class="h-12 w-12 mb-4 mx-auto">
              <h3 class="text-xl font-semibold mb-4 text-red-500">請求書発行の自動化</h3>
              <div class="flex flex-col md:flex-row justify-between items-center mb-4">
                <div class="bg-red-100 p-4 rounded-lg mb-4 md:mb-0 md:mr-4 flex-1">
                  <h4 class="font-semibold text-red-700 mb-2">現状</h4>
                  <p>請求書の発行が手動で行われており、計算ミスや送付の遅れが発生しやすい。</p>
                </div>
                <div class="bg-green-100 p-4 rounded-lg flex-1">
                  <h4 class="font-semibold text-green-700 mb-2">解決策</h4>
                  <p>自動で請求書を生成し、電子メールで送付できるシステムを導入。契約内容や工事の進捗に応じて自動的に金額を計算し、請求書を作成。</p>
                </div>
              </div>
              <div class="bg-blue-100 p-4 rounded-lg">
                <h4 class="font-semibold text-blue-700 mb-2">効果</h4>
                <p>請求書発行業務の効率化、ミスの削減、迅速な支払い回収が実現。</p>
              </div>
            </div>
            
            <div class="bg-gray-100 p-6 rounded-lg shadow-md transform hover:scale-105 transition-all duration-300">
              <img src="/images/労務管理のシステム化.svg" alt="労務管理のシステム化" class="h-12 w-12 mb-4 mx-auto">
              <h3 class="text-xl font-semibold mb-4 text-red-500">労務管理のシステム化</h3>
              <div class="flex flex-col md:flex-row justify-between items-center mb-4">
                <div class="bg-red-100 p-4 rounded-lg mb-4 md:mb-0 md:mr-4 flex-1">
                  <h4 class="font-semibold text-red-700 mb-2">現状</h4>
                  <p>労務時間の管理が手作業やエクセルで行われており、正確な管理が難しい。</p>
                </div>
                <div class="bg-green-100 p-4 rounded-lg flex-1">
                  <h4 class="font-semibold text-green-700 mb-2">解決策</h4>
                  <p>労務管理システムを導入し、現場からモバイルで出退勤を報告。労働時間や休憩時間をリアルタイムで把握できるようにし、給与計算と連携。</p>
                </div>
              </div>
              <div class="bg-blue-100 p-4 rounded-lg">
                <h4 class="font-semibold text-blue-700 mb-2">効果</h4>
                <p>正確な労務管理ができるようになり、給与計算の効率化と人件費の管理が容易になる。</p>
              </div>
            </div>
          </div>
          <div class="text-center">
            <a href="#contact" class="bg-green-500 hover:bg-green-600 text-white font-bold py-3 px-6 rounded-full text-lg transition duration-300 ease-in-out transform hover:scale-105" @click.prevent="scrollToElement('#contact')">
              今すぐ無料相談
            </a>
          </div>
        </div>
      </section>
  
      <!-- Service Overview -->
      <section id="service" class="bg-gray-100 py-16 px-4">
        <div class="container mx-auto">
          <h2 class="text-3xl font-bold mb-8 text-center text-green-500">DXコンサルティングで、貴社の成長を加速</h2>
          <p class="text-lg mb-8 text-center max-w-3xl mx-auto">
            株式会社KOPSは、不動産業、建設業、清掃業などの小規模事業者を対象に、デジタル化を通じた業務効率化とコスト削減をサポートします。大規模プロジェクトで培ったノウハウを、月額29,800円で、小規模企業でも実現可能な形でご提案します。
          </p>
          <div class="grid md:grid-cols-3 gap-8 mb-12">
            <div class="bg-white p-6 rounded-lg shadow-md">
              <img src="/images/低価格.svg" alt="低価格" class="h-12 w-12 mb-4 mx-auto">
              <h3 class="text-xl font-semibold mb-4">低価格</h3>
              <p>月額29,800円のリーズナブルな価格設定</p>
            </div>
            <div class="bg-white p-6 rounded-lg shadow-md">
              <img src="/images/即レスポンス.svg" alt="即レスポンス" class="h-12 w-12 mb-4 mx-auto">
              <h3 class="text-xl font-semibold mb-4">即レスポンス</h3>
              <p>迅速な対応でお客様の問題を即座に解決</p>
            </div>
            <div class="bg-white p-6 rounded-lg shadow-md">
              <img src="/images/幅広い業務対応.svg" alt="幅広い業務対応" class="h-12 w-12 mb-4 mx-auto">
              <h3 class="text-xl font-semibold mb-4">幅広い業務対応</h3>
              <p>WEBサイト構築・運用、業務効率化支援、ITシステム導入代行、独自のシステム開発など、さまざまなサービスを提供。
                ITに関わる業務はすべて丸投げ。
              </p>
            </div>
          </div>
          <div class="text-center">
            <a href="#contact" class="bg-green-500 hover:bg-green-600 text-white font-bold py-3 px-6 rounded-full text-lg transition duration-300 ease-in-out transform hover:scale-105" @click.prevent="scrollToElement('#contact')">
              今すぐ無料相談
            </a>
          </div>
        </div>
      </section>
  
      <!-- Service Flow -->
      <section id="flow" class="bg-white py-16 px-4">
        <div class="container mx-auto">
          <h2 class="text-3xl font-bold mb-12 text-center text-green-500">サービスの流れ</h2>
          <div class="grid md:grid-cols-4 gap-8">
            <div class="bg-gray-100 p-6 rounded-lg shadow-md">
              <img src="/images/現状分析と課題ヒアリング.svg" alt="現状分析と課題ヒアリング" class="h-12 w-12 mb-4 mx-auto">
              <h3 class="text-xl font-semibold mb-4">1. 現状分析と課題ヒアリング</h3>
              <p>業務内容や課題を詳細にヒアリングし、現在の業務状況を分析します。</p>
            </div>
            <div class="bg-gray-100 p-6 rounded-lg shadow-md">
              <img src="/images/最適な提案.svg" alt="最適な提案" class="h-12 w-12 mb-4 mx-auto">
              <h3 class="text-xl font-semibold mb-4">2. 最適な提案</h3>
              <p>あなたの企業に最適なデジタル化の方法を提案します。お客様が気づいていない課題も浮き彫りにします。</p>
            </div>
            <div class="bg-gray-100 p-6 rounded-lg shadow-md">
              <img src="/images/実行支援.svg" alt="実行支援" class="h-12 w-12 mb-4 mx-auto">
              <h3 class="text-xl font-semibold mb-4">3. 実行支援</h3>
              <p>提案内容を実行し、システム導入や業務の改善を支援します。</p>
            </div>
            <div class="bg-gray-100 p-6 rounded-lg shadow-md">
              <img src="/images/継続的なサポート.svg" alt="継続的なサポート" class="h-12 w-12 mb-4 mx-auto">
              <h3 class="text-xl font-semibold mb-4">4. 継続的なサポート</h3>
              <p>実行後もサポートを継続し、必要に応じてさらなる改善を行います。常に伴走し続けるパートナーとなります。</p>
            </div>
          </div>
          <div class="text-center mt-12">
            <a href="#contact" class="bg-green-500 hover:bg-green-600 text-white font-bold py-3 px-6 rounded-full text-lg transition duration-300 ease-in-out transform hover:scale-105" @click.prevent="scrollToElement('#contact')">
              無料相談はこちら
            </a>
          </div>
        </div>
      </section>
  
      <!-- Achievements -->
      <section id="achievements" class="bg-gray-100 py-16 px-4">
        <div class="container mx-auto">
          <h2 class="text-3xl font-bold mb-12 text-center text-green-500">圧倒的な実績</h2>
          <div class="grid md:grid-cols-3 gap-8 mb-12">
            <div class="bg-white p-6 rounded-lg shadow-lg border-2 border-green-500 transform hover:scale-105 transition-transform duration-300">
              <div class="flex items-center justify-between mb-4">
                <h3 class="text-xl font-semibold">生成AIの導入による業務効率化</h3>
                <span class="text-3xl font-bold text-green-500">92%</span>
              </div>
              <p class="text-gray-700">自社独自の生成AIを導入したおかげで、これまで1時間かかっていた調査が5分足らずで済むようになった。</p>
              <div class="mt-4 bg-green-100 p-2 rounded-md">
                <span class="font-semibold text-green-700">調査時間削減率：92%</span>
              </div>
            </div>
            <div class="bg-white p-6 rounded-lg shadow-lg border-2 border-green-500 transform hover:scale-105 transition-transform duration-300">
              <div class="flex items-center justify-between mb-4">
                <h3 class="text-xl font-semibold">GASを活用した業務自動化</h3>
                <span class="text-3xl font-bold text-green-500">67%</span>
              </div>
              <p class="text-gray-700">メール提案活動の自動化を実現。作業時間を1/3に削減した実績。</p>
              <div class="mt-4 bg-green-100 p-2 rounded-md">
                <span class="font-semibold text-green-700">作業時間削減率：67%</span>
              </div>
            </div>
            <div class="bg-white p-6 rounded-lg shadow-lg border-2 border-green-500 transform hover:scale-105 transition-transform duration-300">
              <div class="flex items-center justify-between mb-4">
                <h3 class="text-xl font-semibold">WEBサイトリニューアル</h3>
                <span class="text-3xl font-bold text-green-500">100%</span>
              </div>
              <p class="text-gray-700">SEO強化で問い合わせ数が倍増した事例。</p>
              <div class="mt-4 bg-green-100 p-2 rounded-md">
                <span class="font-semibold text-green-700">問い合わせ増加率：100%</span>
              </div>
            </div>
          </div>
          <div class="text-center">
            <a href="#contact" class="bg-green-500 hover:bg-green-600 text-white font-bold py-3 px-6 rounded-full text-lg transition duration-300 ease-in-out transform hover:scale-105 shadow-xl" @click.prevent="scrollToElement('#contact')">
              圧倒的な実績を体験する
            </a>
          </div>
        </div>
      </section>
  
      <!-- Customer Reviews -->
      <section id="reviews" class="bg-white py-16 px-4">
        <div class="container mx-auto">
          <h2 class="text-3xl font-bold mb-12 text-center text-green-500">お客様の声</h2>
          <div class="grid md:grid-cols-2 gap-8 mb-12">
            <div class="relative bg-white p-6 rounded-lg shadow-md">
              <div class="absolute top-0 left-0 w-0 h-0 border-t-[20px] border-l-[20px] border-t-green-500 border-l-transparent"></div>
              <div class="bg-green-100 p-4 rounded-lg mb-4">
                <p class="mb-2">「丁寧なヒアリングで、私たちが気づいていなかった課題を発見し、最適な解決策を提案してもらいました。」</p>
              </div>
              <p class="font-semibold text-right">- A社 代表取締役</p>
            </div>
            <div class="relative bg-white p-6 rounded-lg shadow-md">
              <div class="absolute top-0 left-0 w-0 h-0 border-t-[20px] border-l-[20px] border-t-green-500 border-l-transparent"></div>
              <div class="bg-green-100 p-4 rounded-lg mb-4">
                <p class="mb-2">「DX導入後、業務効率が飛躍的に向上しました。サポートがとても迅速で助かっています。」</p>
              </div>
              <p class="font-semibold text-right">- B社 経営企画部長</p>
            </div>
          </div>
          <div class="text-center">
            <a href="#contact" class="bg-green-500 hover:bg-green-600 text-white font-bold py-3 px-6 rounded-full text-lg transition duration-300 ease-in-out transform hover:scale-105" @click.prevent="scrollToElement('#contact')">
              今すぐ無料相談
            </a>
          </div>
        </div>
      </section>
  
      <!-- Consultant Introduction -->
      <section id="consultant" class="bg-gray-100 py-16 px-4">
        <div class="container mx-auto">
          <h2 class="text-3xl font-bold mb-12 text-center text-green-500">あなたのDX顧問 - 馬込 浩</h2>
          <div class="flex flex-col md:flex-row items-center justify-center">
            <img src="/リサイズ浩.png" alt="馬込 浩" class="rounded-full w-64 h-64 object-cover mb-8 md:mb-0 md:mr-12" />
            <div class="max-w-lg">
              <p class="text-lg mb-8">
                新進気鋭のベンチャー企業から、グロース上場企業、プライム上場企業（時価総額ベスト5以内企業）まで多数のプロジェクトで、開発、プロジェクトマネジメント支援、ITコンサルティングを行ってきました。
                ITシステムの導入や業務効率化の実績を多数持ち、どのような課題にも迅速に対応いたします。
              </p>
              <div class="flex flex-col sm:flex-row justify-center items-center space-y-4 sm:space-y-0 sm:space-x-4">
                <a href="#contact" class="bg-green-500 hover:bg-green-600 text-white font-bold py-3 px-6 rounded-full text-lg transition duration-300 ease-in-out transform hover:scale-105" @click.prevent="scrollToElement('#contact')">
                  今すぐ無料相談
                </a>
                <a href="https://even-wheel-148.notion.site/275c8bd3ec004fe18061816694d39726" target="_blank" rel="noopener noreferrer" class="bg-blue-500 hover:bg-blue-600 text-white font-bold py-3 px-6 rounded-full text-lg transition duration-300 ease-in-out transform hover:scale-105">
                  詳細なプロフィール
                </a>
              </div>
            </div>
          </div>
        </div>
      </section>
  
      <!-- FAQ -->
      <section class="bg-white py-16 px-4">
        <div class="container mx-auto">
          <h2 class="text-3xl font-bold mb-12 text-center text-green-500">よくある質問</h2>
          <div class="max-w-3xl mx-auto">
            <div class="mb-8">
              <h3 class="text-xl font-semibold mb-2">DXって何ですか？</h3>
              <p>DXとはデジタルトランスフォーメーションの略で、デジタル技術を活用して業務効率を上げ、新たなビジネス価値を創造する取り組みです。</p>
            </div>
            <div class="mb-8">
              <h3 class="text-xl font-semibold mb-2">どのような企業が対象ですか？</h3>
              <p>主に1～20名規模の不動産業、建設業、清掃業など、業務効率化やデジタル化を考えている企業様が対象です。</p>
            </div>
            <div class="mb-8">
              <h3 class="text-xl font-semibold mb-2">相談だけでも大丈夫ですか？</h3>
              <p>全く問題ありません。まずはお気軽にご相談ください。ご相談の中でご自身が思いつかないような解決策を提示する場合も多くあります。</p>
            </div>
          </div>
          <div class="text-center mt-12">
            <a href="#contact" class="bg-green-500 hover:bg-green-600 text-white font-bold py-3 px-6 rounded-full text-lg transition duration-300 ease-in-out transform hover:scale-105" @click.prevent="scrollToElement('#contact')">
              今すぐ無料相談
            </a>
          </div>
        </div>
      </section>

      <!-- Contact Form -->
      <section id="contact" class="bg-gray-100 py-16 px-4">
        <div class="container mx-auto">
          <h2 class="text-3xl font-bold mb-12 text-center text-green-500">今すぐ無料相談をお申し込みください</h2>
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
  
      <!-- Footer -->
      <footer class="bg-gray-800 text-white py-8 px-4">
        <div class="container mx-auto text-center">
          <div class="mb-8">
            <h3 class="text-xl font-semibold mb-4 cursor-pointer hover:text-gray-300 transition duration-300 ease-in-out" @click="scrollToTop">あなたのDX顧問</h3>
            <ul class="flex flex-wrap justify-center space-x-4">
              <li><a href="#service" class="hover:text-gray-300 transition duration-300 ease-in-out" @click.prevent="scrollToElement('#service')">サービス概要</a></li>
              <li><a href="#flow" class="hover:text-gray-300 transition duration-300 ease-in-out" @click.prevent="scrollToElement('#flow')">サービスの流れ</a></li>
              <li><a href="#achievements" class="hover:text-gray-300 transition duration-300 ease-in-out" @click.prevent="scrollToElement('#achievements')">実績紹介</a></li>
              <li><a href="#reviews" class="hover:text-gray-300 transition duration-300 ease-in-out" @click.prevent="scrollToElement('#reviews')">お客様の声</a></li>
              <li><a href="#consultant" class="hover:text-gray-300 transition duration-300 ease-in-out" @click.prevent="scrollToElement('#consultant')">DXコンサルタント</a></li>
              <li><a href="#contact" class="hover:text-gray-300 transition duration-300 ease-in-out" @click.prevent="scrollToElement('#contact')">お問い合わせ</a></li>
            </ul>
          </div>
          <div class="border-t border-gray-700 pt-8">
            <h3 class="text-xl font-semibold mb-4">運営会社</h3>
            <div class="text-left max-w-fit mx-auto">
              <p>株式会社KOPS</p>
              <p>住所: 千葉県船橋市前原西2-14-2 津田沼駅前安田ビル別館2階26</p>
            </div>
            <p class="mt-4">&copy; 2024 株式会社KOPS All Rights Reserved.</p>
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

const scrollToElement = (selector) => {
  const element = document.querySelector(selector)
  if (element) {
    element.scrollIntoView({ behavior: 'smooth' })
  }
}

const scrollToTop = () => {
  window.scrollTo({
    top: 0,
    behavior: 'smooth'
  })
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