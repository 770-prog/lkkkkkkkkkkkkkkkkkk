<!-- 디바이스 상단 스테이터스 바 디자인 (데스크톱 데코레이션) -->
<div class="hidden sm:flex justify-between items-center px-8 pt-3 pb-2 bg-white text-xs font-semibold text-neutral-500 select-none z-40">
  <span>10:39</span>
  <div class="w-20 h-4 bg-neutral-900 rounded-full mx-auto absolute left-1/2 -translate-x-1/2 top-3"></div>
  <div class="flex gap-1.5 items-center">
    <span class="text-[9px] bg-emerald-100 text-emerald-700 px-1.5 py-0.5 rounded-full font-bold">E2EE</span>
    <span>LTE</span>
  </div>
</div>

<!-- [APP VIEWS] -->

<!-- 1. 로그인 뷰 -->
<div id="view-login" class="flex-1 flex flex-col justify-between p-8 bg-gradient-to-b from-neutral-50 to-white z-10">
  <div class="my-auto space-y-8">
    <div class="text-center space-y-3">
      <div class="w-16 h-16 bg-neutral-900 text-white rounded-2xl flex items-center justify-center mx-auto mb-4 shadow-md">
        <!-- BookOpen Icon SVG -->
        <svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round"><path d="M2 3h6a4 4 0 0 1 4 4v14a3 3 0 0 0-3-3H2z"/><path d="M22 3h-6a4 4 0 0 0-4 4v14a3 3 0 0 1 3-3h7z"/></svg>
      </div>
      <h1 class="text-3xl font-extrabold tracking-tight text-neutral-900">EducatedTalk</h1>
      <p class="text-neutral-500 text-sm">교육용 안심 1:1 멘토링 및 클린 DM 시스템</p>
    </div>

    <form id="login-form" class="space-y-4">
      <div class="space-y-2">
        <label class="text-xs font-bold text-neutral-500 uppercase tracking-wider">로그인 및 인증</label>
        <div class="relative">
          <div class="absolute inset-y-0 left-0 pl-4 flex items-center pointer-events-none text-neutral-400 gap-1.5">
            <!-- Mail & Phone Dual Icon Representation -->
            <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><rect width="20" height="16" x="2" y="4" rx="2"/><path d="m22 7-8.97 5.7a1.94 1.94 0 0 1-2.06 0L2 7"/></svg>
            <span class="text-neutral-300">|</span>
            <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><rect width="14" height="20" x="5" y="2" rx="2" ry="2"/><path d="M12 18h.01"/></svg>
          </div>
          <input
            type="text"
            id="login-input"
            placeholder="이메일 또는 휴대폰 번호 입력"
            class="w-full pl-20 pr-4 py-4 bg-neutral-50 border border-neutral-200 rounded-2xl focus:outline-none focus:ring-2 focus:ring-neutral-900 focus:border-transparent transition-all text-sm"
          />
        </div>
        <p id="login-error" class="text-xs text-red-500 flex items-center gap-1 mt-1 hidden">
          <!-- Warning Icon -->
          <svg xmlns="http://www.w3.org/2000/svg" width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="inline"><path d="m21.73 18-8-14a2 2 0 0 0-3.48 0l-8 14A2 2 0 0 0 4 21h16a2 2 0 0 0 1.73-3Z"/><line x1="12" y1="9" x2="12" y2="13"/><line x1="12" y1="17" x2="12.01" y2="17"/></svg>
          <span id="login-error-text">오류 메시지</span>
        </p>
      </div>

      <button
        type="submit"
        class="w-full bg-neutral-950 hover:bg-neutral-800 text-white font-semibold py-4 rounded-2xl transition-all shadow-md active:scale-95"
      >
        시작하기
      </button>
    </form>
  </div>

  <div class="text-center text-xs text-neutral-400 space-y-1.5 border-t border-neutral-100 pt-6">
    <div class="flex items-center justify-center gap-1 text-neutral-500 font-semibold mb-1">
      <!-- Sparkle Icon -->
      <svg xmlns="http://www.w3.org/2000/svg" width="12" height="12" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="text-neutral-500"><path d="m12 3-1.912 5.813a2 2 0 0 1-1.275 1.275L3 12l5.813 1.912a2 2 0 0 1 1.275 1.275L12 21l1.912-5.813a2 2 0 0 1 1.275-1.275L21 12l-5.813-1.912a2 2 0 0 1-1.275-1.275Z"/></svg>
      <span>에듀케이트톡 클린 원칙</span>
    </div>
    <p>본 메신저는 불특정 다수의 그룹 채팅을 지원하지 않습니다.</p>
    <p>공개 피드, 스토리, 메모 및 가짜 가입자 유도가 없습니다.</p>
  </div>
</div>

<!-- 2. 메인 앱 레이아웃 (로그인 후 노출) -->
<div id="view-main" class="flex-1 flex flex-col bg-neutral-50 h-full overflow-hidden hidden">
  
  <!-- 공통 상단 헤더 -->
  <header id="main-header" class="px-6 py-4 bg-white border-b border-neutral-100 flex justify-between items-center z-10">
    <div>
      <span class="text-[10px] text-neutral-400 font-extrabold uppercase tracking-widest">EducatedTalk</span>
      <h1 id="header-title" class="text-2xl font-black text-neutral-950">EduChat</h1>
    </div>
    <button 
      id="btn-add-follower" 
      class="p-2.5 bg-neutral-100 text-neutral-900 rounded-full hover:bg-neutral-200 transition active:scale-95 hidden"
    >
      <!-- UserPlus Icon -->
      <svg xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M16 21v-2a4 4 0 0 0-4-4H6a4 4 0 0 0-4 4v2"/><circle cx="9" cy="7" r="4"/><line x1="19" y1="8" x2="19" y2="14"/><line x1="22" y1="11" x2="16" y2="11"/></svg>
    </button>
  </header>

  <!-- 스크롤 가능 본문 영역 -->
  <div id="main-content" class="flex-1 overflow-y-auto hide-scrollbar relative">
    
    <!-- 하위 뷰 A: 팔로워 관리 -->
    <div id="subview-followers" class="p-4 space-y-4 hidden fade-in">
      <!-- 비었을 때 화면 -->
      <div id="followers-empty" class="flex flex-col items-center justify-center py-24 text-center space-y-4">
        <div class="w-16 h-16 bg-neutral-100 rounded-full flex items-center justify-center text-neutral-300">
          <svg xmlns="http://www.w3.org/2000/svg" width="28" height="28" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M19 21v-2a4 4 0 0 0-4-4H9a4 4 0 0 0-4 4v2"/><circle cx="12" cy="7" r="4"/></svg>
        </div>
        <div class="space-y-1">
          <h3 class="font-bold text-neutral-800">등록된 팔로워가 없습니다</h3>
          <p class="text-xs text-neutral-400">우측 상단 버튼을 클릭해 대화할<br />멘토 또는 학생을 등록해보세요.</p>
        </div>
      </div>
      <!-- 목록 화면 -->
      <div id="followers-list-container" class="space-y-2 hidden">
        <span class="text-[11px] font-bold text-neutral-400 uppercase px-1">전체 팔로워 (<span id="followers-count">0</span>)</span>
        <ul id="followers-list" class="space-y-2"></ul>
      </div>
    </div>

    <!-- 하위 뷰 B: 1:1 대화방 목록 -->
    <div id="subview-educhat" class="p-4 space-y-4 fade-in">
      <!-- 비었을 때 화면 -->
      <div id="chats-empty" class="flex flex-col items-center justify-center py-24 text-center space-y-4">
        <div class="w-16 h-16 bg-neutral-100 rounded-full flex items-center justify-center text-neutral-300">
          <svg xmlns="http://www.w3.org/2000/svg" width="28" height="28" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M21 15a2 2 0 0 1-2 2H7l-4 4V5a2 2 0 0 1 2-2h14a2 2 0 0 1 2 2z"/></svg>
        </div>
        <div class="space-y-1">
          <h3 class="font-bold text-neutral-800">대화방이 활성화되지 않았습니다</h3>
          <p class="text-xs text-neutral-400">팔로워 메뉴에서 대화 상대를 선택해<br />안심 1:1 대화를 진행해보세요.</p>
        </div>
      </div>
      <!-- 목록 화면 -->
      <div id="chats-list-container" class="space-y-2 hidden">
        <span class="text-[11px] font-bold text-neutral-400 uppercase px-1">진행중인 1:1 대화 (<span id="chats-count">0</span>)</span>
        <ul id="chats-list" class="space-y-2"></ul>
      </div>
    </div>

    <!-- 하위 뷰 C: 설정 페이지 -->
    <div id="subview-settings" class="p-5 space-y-5 hidden fade-in">
      <div class="bg-white rounded-2xl p-5 border border-neutral-100 shadow-sm flex items-center gap-4">
        <div id="settings-avatar" class="w-14 h-14 bg-neutral-950 text-white font-extrabold rounded-2xl flex items-center justify-center text-xl">
          U
        </div>
        <div>
          <h3 id="settings-username" class="font-bold text-neutral-900 text-lg">Username</h3>
          <p id="settings-contact" class="text-xs text-neutral-400">Contact Info</p>
        </div>
      </div>

      <div class="bg-white rounded-2xl border border-neutral-100 shadow-sm overflow-hidden text-sm">
        <div class="p-4 border-b border-neutral-100 flex justify-between items-center">
          <span class="font-semibold text-neutral-700">종단간 암호화(E2EE)</span>
          <span class="text-xs bg-emerald-100 text-emerald-800 px-2 py-0.5 rounded-full font-bold">활성화됨</span>
        </div>
        <div class="p-4 border-b border-neutral-100 flex justify-between items-center text-neutral-700">
          <span>가입 수단</span>
          <span id="settings-method" class="text-xs text-neutral-500 font-semibold">이메일 인증</span>
        </div>
        <div class="p-4 border-b border-neutral-100 flex justify-between items-center text-neutral-700">
          <span>어플리케이션 버전</span>
          <span class="text-xs text-neutral-400 font-mono">v1.1.0-secure-html</span>
        </div>
        <button 
          id="btn-logout"
          class="w-full p-4 text-left text-red-500 hover:bg-red-50 transition flex items-center gap-2 font-bold"
        >
          <!-- LogOut Icon -->
          <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M9 21H5a2 2 0 0 1-2-2V5a2 2 0 0 1 2-2h4"/><polyline points="16 17 21 12 16 7"/><line x1="21" y1="12" x2="9" y2="12"/></svg>
          계정 로그아웃
        </button>
      </div>
    </div>

  </div>

  <!-- 공통 하단 네비게이션 탭 바 -->
  <nav class="bg-white border-t border-neutral-100 py-3.5 px-8 flex justify-between items-center z-10">
    <button 
      id="tab-followers"
      class="flex flex-col items-center gap-1.5 transition-all text-neutral-400 hover:text-neutral-600"
    >
      <svg xmlns="http://www.w3.org/2000/svg" width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M19 21v-2a4 4 0 0 0-4-4H9a4 4 0 0 0-4 4v2"/><circle cx="12" cy="7" r="4"/></svg>
      <span class="text-[9px] font-bold">팔로워</span>
    </button>
    
    <button 
      id="tab-educhat"
      class="flex flex-col items-center gap-1.5 transition-all text-neutral-950 scale-105 relative"
    >
      <svg xmlns="http://www.w3.org/2000/svg" width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M21 15a2 2 0 0 1-2 2H7l-4 4V5a2 2 0 0 1 2-2h14a2 2 0 0 1 2 2z"/></svg>
      <span id="badge-dot" class="absolute top-0 right-1.5 w-2 h-2 bg-emerald-500 rounded-full border-2 border-white hidden"></span>
      <span class="text-[9px] font-bold">EduChat</span>
    </button>

    <button 
      id="tab-settings"
      class="flex flex-col items-center gap-1.5 transition-all text-neutral-400 hover:text-neutral-600"
    >
      <svg xmlns="http://www.w3.org/2000/svg" width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="12" r="3"/><path d="M19.4 15a1.65 1.65 0 0 0 .33 1.82l.06.06a2 2 0 1 1-2.83 2.83l-.06-.06a1.65 1.65 0 0 0-1.82-.33 1.65 1.65 0 0 0-1 1.51V21a2 2 0 0 1-4 0v-.09A1.65 1.65 0 0 0 9 19.4a1.65 1.65 0 0 0-1.82.33l-.06.06a2 2 0 1 1-2.83-2.83l.06-.06a1.65 1.65 0 0 0 .33-1.82 1.65 1.65 0 0 0-1.51-1H3a2 2 0 0 1 0-4h.09A1.65 1.65 0 0 0 4.6 9a1.65 1.65 0 0 0-.33-1.82l-.06-.06a2 2 0 1 1 2.83-2.83l.06.06a1.65 1.65 0 0 0 1.82.33H9a1.65 1.65 0 0 0 1-1.51V3a2 2 0 0 1 4 0v.09a1.65 1.65 0 0 0 1 1.51 1.65 1.65 0 0 0 1.82-.33l.06-.06a2 2 0 1 1 2.83 2.83l-.06.06a1.65 1.65 0 0 0-.33 1.82V9a1.65 1.65 0 0 0 1.51 1H21a2 2 0 0 1 0 4h-.09a1.65 1.65 0 0 0-1.51 1z"/></svg>
      <span class="text-[9px] font-bold">설정</span>
    </button>
  </nav>

</div>

<!-- 3. 1:1 전용 채팅방 내부 레이아웃 (오버레이로 더 부드럽고 가벼운 전환 지원) -->
<div id="view-chat-room" class="absolute inset-0 bg-neutral-50 flex flex-col z-30 hidden fade-in">
  
  <!-- 채팅 헤더 -->
  <header class="px-4 py-4 bg-white border-b border-neutral-100 flex items-center gap-3 sticky top-0 z-10 shadow-sm">
    <button id="btn-back-to-list" class="p-1.5 hover:bg-neutral-100 rounded-full transition">
      <!-- ArrowLeft Icon -->
      <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="text-neutral-900"><line x1="19" y1="12" x2="5" y2="12"/><polyline points="12 19 5 12 12 5"/></svg>
    </button>
    <div class="flex items-center gap-2.5">
      <div id="chat-room-avatar" class="w-9 h-9 bg-neutral-900 text-white rounded-lg flex items-center justify-center font-bold text-sm">
        T
      </div>
      <div>
        <h3 id="chat-room-title" class="font-bold text-neutral-900 text-sm leading-none mb-1">상대방 닉네임</h3>
        <p class="text-[10px] text-emerald-600 font-semibold flex items-center gap-0.5">
          <span class="w-1.5 h-1.5 bg-emerald-500 rounded-full animate-pulse"></span> 1:1 보안 서신
        </p>
      </div>
    </div>
  </header>

  <!-- 메시지 바디 -->
  <div id="chat-messages-container" class="flex-1 overflow-y-auto p-4 space-y-4">
    <div class="text-center my-4">
      <span id="chat-date-badge" class="px-3 py-1 bg-neutral-200/50 text-neutral-500 text-[10px] font-bold rounded-full uppercase tracking-wider">
        안전 대화 채널 개설됨
      </span>
    </div>
    <div id="chat-messages-list" class="space-y-4"></div>
    <div id="chat-anchor"></div>
  </div>

  <!-- 전송 하단 바 -->
  <footer class="p-3 bg-white border-t border-neutral-100">
    <form id="message-form" class="flex gap-2">
      <input
        type="text"
        id="message-input"
        placeholder="전달할 메시지를 입력하세요..."
        autocomplete="off"
        class="flex-1 px-4 py-3 bg-neutral-50 border border-neutral-200 rounded-xl text-sm outline-none focus:bg-white focus:border-neutral-400 transition"
      />
      <button 
        type="submit" 
        class="p-3 bg-neutral-950 text-white rounded-xl hover:bg-neutral-800 transition flex items-center justify-center"
      >
        <!-- Send Icon -->
        <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><line x1="22" y1="2" x2="11" y2="13"/><polygon points="22 2 15 22 11 13 2 9 22 2"/></svg>
      </button>
    </form>
  </footer>

</div>

<!-- 새 팔로워 추가 모달 대화창 -->
<div id="add-follower-modal" class="absolute inset-0 bg-neutral-950/60 backdrop-blur-xs z-50 flex items-center justify-center p-4 hidden">
  <div class="bg-white rounded-3xl w-full max-w-[340px] shadow-2xl p-6 space-y-4 transform scale-95 transition-all">
    <div class="space-y-1">
      <h3 class="text-lg font-bold text-neutral-900">대화 상대 직접 추가</h3>
      <p class="text-xs text-neutral-400">아이디 또는 성함을 입력하여 팔로워에 추가합니다.</p>
    </div>

    <form id="add-follower-form" class="space-y-3">
      <div class="relative">
        <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="absolute left-3 top-1/2 -translate-y-1/2 text-neutral-400"><circle cx="11" cy="11" r="8"/><line x1="21" y1="21" x2="16.65" y2="16.65"/></svg>
        <input 
          type="text"
          id="follower-search-input"
          placeholder="사용자명 입력 (예: 홍길동교사)" 
          class="w-full bg-neutral-50 border border-neutral-200 rounded-xl py-2.5 pl-9 pr-3 text-sm outline-none focus:ring-2 focus:ring-neutral-900 focus:border-transparent transition"
        />
      </div>
      <p id="follower-error" class="text-[11px] text-red-500 font-semibold hidden">에러 메시지</p>
      <div class="flex gap-2 pt-2">
        <button 
          type="button"
          id="btn-close-modal"
          class="flex-1 py-2.5 bg-neutral-100 text-neutral-700 text-xs font-semibold rounded-xl hover:bg-neutral-200 transition"
        >
          취소
        </button>
        <button 
          type="submit"
          class="flex-1 py-2.5 bg-neutral-950 text-white text-xs font-semibold rounded-xl hover:bg-neutral-800 transition"
        >
          목록에 등록
        </button>
      </div>
    </form>
  </div>
</div>
