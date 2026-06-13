<script>
  let { whatsappNumber } = $props();

  function generateWaLink(serviceName, rate) {
    const text = `Hello Sorecare, I would like to book the ${serviceName} plan (${rate}/hour). Please guide me to the next steps.`;
    return `https://wa.me/${whatsappNumber}?text=${encodeURIComponent(text)}`;
  }
</script>

<div class="grid grid-cols-1 md:grid-cols-3 gap-8 max-w-4xl mx-auto">
  <!-- Standard Care -->
  <div class="bg-white border border-zinc-100 rounded-3xl p-8 flex flex-col justify-between shadow-sm relative overflow-hidden">
    <div>
      <h3 class="text-zinc-900 font-serif text-xl font-medium">Standard Care</h3>
      <p class="text-zinc-400 text-xs mt-1">Caregiver & Fresh Graduates</p>
      <div class="mt-6 flex items-baseline text-zinc-900">
        <span class="text-2xl font-semibold tracking-tight">IDR</span>
        <span class="text-5xl font-serif font-bold tracking-tight ml-1">60K</span>
        <span class="text-zinc-400 text-sm ml-1">/ hour</span>
      </div>
      <ul class="mt-8 space-y-4 text-sm text-zinc-600">
        <li class="flex items-center gap-2">✓ Elderly companionship</li>
        <li class="flex items-center gap-2">✓ Daily mobility assistance</li>
        <li class="flex items-center gap-2">✓ Meal & bath assistance</li>
      </ul>
    </div>
    <div class="mt-8">
      <a href={generateWaLink('Standard Care', 'IDR 60K')} target="_blank" class="block w-full text-center font-medium bg-zinc-900 text-white py-3 rounded-xl hover:bg-zinc-800 transition-all text-sm">
        Book Standard
      </a>
    </div>
  </div>

  <!-- Intensive Care -->
  <div class="bg-white border-2 border-[#1b4332] rounded-3xl p-8 flex flex-col justify-between shadow-md relative overflow-hidden">
    <div class="absolute top-0 right-0 bg-[#1b4332] text-white text-[10px] uppercase font-bold tracking-widest px-4 py-1 rounded-bl-xl">
      Most Requested
    </div>
    <div>
      <h3 class="text-zinc-900 font-serif text-xl font-medium">Intensive Care</h3>
      <p class="text-zinc-400 text-xs mt-1">Registered Nurse (Ber-STR)</p>
      <div class="mt-6 flex items-baseline text-zinc-900">
        <span class="text-2xl font-semibold tracking-tight">IDR</span>
        <span class="text-5xl font-serif font-bold tracking-tight ml-1">70K</span>
        <span class="text-zinc-400 text-sm ml-1">/ hour</span>
      </div>
      <ul class="mt-8 space-y-4 text-sm text-zinc-600">
        <li class="flex items-center gap-2">✓ Post-surgery recovery</li>
        <li class="flex items-center gap-2">✓ Advanced wound care</li>
        <li class="flex items-center gap-2">✓ Vital signs & medical monitoring</li>
      </ul>
    </div>
    <div class="mt-8">
      <a href={generateWaLink('Intensive Care', 'IDR 70K')} target="_blank" class="block w-full text-center font-medium bg-[#1b4332] text-white py-3 rounded-xl hover:bg-[#143225] transition-all text-sm">
        Book Intensive
      </a>
    </div>
  </div>

  <!-- Night Shift Premium -->
  <div class="bg-white border border-zinc-100 rounded-3xl p-8 flex flex-col justify-between shadow-sm relative overflow-hidden">
    <div>
      <h3 class="text-zinc-900 font-serif text-xl font-medium">Night Shift</h3>
      <p class="text-zinc-400 text-xs mt-1">Overnight Standby Care</p>
      <div class="mt-6 flex items-baseline text-zinc-900">
        <span class="text-2xl font-semibold tracking-tight">IDR</span>
        <span class="text-5xl font-serif font-bold tracking-tight ml-1">80K</span>
        <span class="text-zinc-400 text-sm ml-1">/ hour</span>
      </div>
      <ul class="mt-8 space-y-4 text-sm text-zinc-600">
        <li class="flex items-center gap-2">✓ 20:00 - 06:00 WITA coverage</li>
        <li class="flex items-center gap-2">✓ Midnight emergency monitoring</li>
        <li class="flex items-center gap-2">✓ Overnight peace of mind</li>
      </ul>
    </div>
    <div class="mt-8">
      <a href={generateWaLink('Night Shift Premium', 'IDR 80K')} target="_blank" class="block w-full text-center font-medium bg-zinc-900 text-white py-3 rounded-xl hover:bg-zinc-800 transition-all text-sm">
        Book Night Shift
      </a>
    </div>
  </div>
</div>