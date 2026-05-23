<script lang="ts">
    // Destructure state handlers passed from the root page view layout pipeline
    let { onPrivacyClick, onTermsClick } = $props();
  </script>
  
  <footer class="w-full bg-white text-slate-900 pt-16 pb-8 px-6 md:px-12 border-t border-slate-100 select-none">
    <div class="max-w-7xl mx-auto w-full flex flex-col space-y-12">
      
      <div class="grid grid-cols-1 md:grid-cols-12 gap-8 items-start">
        
        <div class="md:col-span-4 flex flex-col space-y-3 text-left">
          <h2 class="text-2xl font-black tracking-tight uppercase">
            Sasmit<span class="text-blue-600">.</span>
          </h2>
          <p class="text-sm font-medium text-slate-500 max-w-xs leading-relaxed">
            Building a modern, digital, and accountable Nepal together.
          </p>
        </div>
  
        <div class="md:col-span-5 flex flex-col space-y-3 text-left md:items-center">
          <div class="flex flex-col space-y-2">
            <span class="text-[10px] font-bold uppercase tracking-[0.2em] text-slate-400">
              CONTACT INFO
            </span>
            <a 
              href="mailto:contact@sasmitpokharel.com" 
              class="inline-flex items-center space-x-2 text-sm font-semibold text-slate-700 hover:text-blue-600 transition-colors"
            >
              <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" class="w-4 h-4 text-blue-500">
                <path stroke-linecap="round" stroke-linejoin="round" d="M21.75 6.75v10.5a2.25 2.25 0 0 1-2.25 2.25H4.5A2.25 2.25 0 0 1 2.25 17.25V6.75m19.5 0A2.25 2.25 0 0 0 19.5 4.5H4.5a2.25 2.25 0 0 0-2.25 2.25m19.5 0v.243a2.25 2.25 0 0 1-1.07 1.916l-7.5 4.615a2.25 2.25 0 0 1-2.36 0L3.32 8.91a2.25 2.25 0 0 1-1.07-1.916V6.75" />
              </svg>
              <span>contact@sasmitpokharel.com</span>
            </a>
          </div>
        </div>
  
        <div class="md:col-span-3 flex flex-col space-y-3 text-left md:items-end">
          <div class="flex flex-col space-y-2 md:items-end">
            <span class="text-[10px] font-bold uppercase tracking-[0.2em] text-slate-400">
              FOLLOW US
            </span>
            <div class="flex items-center space-x-5 text-slate-700">
              <a href="https://facebook.com" target="_blank" rel="noreferrer" class="hover:text-blue-600 transition-colors" aria-label="Facebook Profile">
                <svg xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M18 2h-3a5 5 0 0 0-5 5v3H7v4h3v8h4v-8h3l1-4h-4V7a1 1 0 0 1 1-1h3z"/></svg>
              </a>
              <a href="https://tiktok.com" target="_blank" rel="noreferrer" class="hover:text-black transition-colors" aria-label="TikTok Profile">
                <svg xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M9 12a4 4 0 1 0 4 4V4a5 5 0 0 0 5 5"/></svg>
              </a>
              <a href="https://instagram.com" target="_blank" rel="noreferrer" class="hover:text-pink-600 transition-colors" aria-label="Instagram Profile">
                <svg xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><rect x="2" y="2" width="20" height="20" rx="5" ry="5"/><path d="M16 11.37A4 4 0 1 1 12.63 8 4 4 0 0 1 16 11.37z"/><line x1="17.5" y1="6.5" x2="17.51" y2="6.5"/></svg>
              </a>
            </div>
          </div>
        </div>
  
      </div>
  
      <div class="pt-8 border-t border-slate-100 flex flex-col sm:flex-row items-center justify-between gap-4 text-xs font-semibold text-slate-400">
        <span>© 2026 Sasmit Pokharel. All rights reserved.</span>
        <div class="flex items-center space-x-6">
          
          <button 
            onclick={onPrivacyClick} 
            class="hover:text-slate-600 transition-colors bg-transparent border-none p-0 cursor-pointer font-semibold text-xs text-slate-400 focus:outline-none"
          >
            Privacy Policy
          </button>
          
          <button 
            onclick={onTermsClick} 
            class="hover:text-slate-600 transition-colors bg-transparent border-none p-0 cursor-pointer font-semibold text-xs text-slate-400 focus:outline-none"
          >
            Terms of Service
          </button>
          
        </div>
      </div>
  
    </div>
  </footer>