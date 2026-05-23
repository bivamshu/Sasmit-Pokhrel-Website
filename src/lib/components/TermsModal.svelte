<script lang="ts">
    // Two-way bindable prop to control visibility from parent component
    let { isOpen = $bindable(false) } = $props();
  
    // Watch open state to manage page body scrolling behavior
    $effect(() => {
      if (isOpen) {
        document.body.style.overflow = 'hidden';
      } else {
        document.body.style.overflow = '';
      }
      return () => {
        document.body.style.overflow = '';
      };
    });
  
    // Terms content mapped directly from design specifications
    const termsSections = [
      {
        title: '1. Acceptance of Terms',
        text: 'By accessing this website, you agree to be bound by these Terms of Service and all applicable laws and regulations.'
      },
      {
        title: '2. Use License',
        text: "Permission is granted to temporarily download one copy of the materials on Sasmit Pokhrel's website for personal, non-commercial transitory viewing only."
      },
      {
        title: '3. Disclaimer',
        text: 'The materials on this website are provided on an "as is" basis. We make no warranties, expressed or implied, and hereby disclaim and negate all other warranties.'
      }
    ];
  </script>
  
  {#if isOpen}
    <div 
      class="fixed inset-0 z-50 bg-slate-900/60 backdrop-blur-sm flex items-center justify-center p-4 select-none animate-fade-in"
      onclick={() => isOpen = false}
      role="presentation"
    >
      
      <div 
        class="bg-white text-slate-900 w-full max-w-2xl rounded-lg shadow-2xl flex flex-col max-h-[85vh] overflow-hidden transition-all duration-300 scale-100"
        onclick={(e) => e.stopPropagation()}
        role="dialog"
        aria-modal="true"
        aria-labelledby="terms-title"
      >
        
        <div class="p-6 md:p-8 border-b border-slate-100 flex items-center justify-between bg-white z-10">
          <h2 id="terms-title" class="text-2xl font-black tracking-tight text-slate-900">
            Terms of Service
          </h2>
          
          <button 
            onclick={() => isOpen = false}
            class="p-2 text-slate-400 hover:text-slate-600 hover:bg-slate-50 rounded-full transition-colors duration-200 focus:outline-none"
            aria-label="Close terms of service"
          >
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2.5" stroke="currentColor" class="w-5 h-5">
              <path stroke-linecap="round" stroke-linejoin="round" d="M6 18 18 6M6 6l12 12" />
            </svg>
          </button>
        </div>
  
        <div class="p-6 md:p-8 overflow-y-auto space-y-6 text-left scrollbar-thin scrollbar-thumb-slate-200">
          {#each termsSections as section}
            <div class="space-y-2">
              <h3 class="text-lg font-bold text-[#00a3ff] tracking-wide">
                {section.title}
              </h3>
              <p class="text-sm md:text-base text-slate-500 font-medium leading-relaxed">
                {section.text}
              </p>
            </div>
          {/each}
          
          <div class="pt-4 border-t border-slate-100 text-xs font-semibold text-slate-400">
            Last updated: February 2026
          </div>
        </div>
  
      </div>
    </div>
  {/if}
  
  <style>
    @keyframes fadeIn {
      from { opacity: 0; }
      to { opacity: 1; }
    }
    .animate-fade-in {
      animation: fadeIn 0.2s ease-out forwards;
    }
  </style>