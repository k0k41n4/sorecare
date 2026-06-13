<script>
  let { whatsappUrl } = $props();

  const talents = [
    { name: "Putu A.", role: "Registered Nurse", exp: "4 Years Exp", status: "Available", img: "🟢" },
    { name: "Ni Ketut S.", role: "Senior Caregiver", exp: "5 Years Exp", status: "On Duty", img: "🔴" },
    { name: "Made W.", role: "ICU Specialist", exp: "6 Years Exp", status: "Available", img: "🟢" },
    { name: "Wayan J.", role: "Elderly Caregiver", exp: "3 Years Exp", status: "On Duty", img: "🔴" }
  ];
</script>

<div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-6">
  {#each talents as talent}
    <div class="bg-white p-6 rounded-2xl border border-zinc-100 shadow-sm flex flex-col justify-between">
      <div>
        <div class="flex justify-between items-start mb-4">
          <div class="w-12 h-12 rounded-xl bg-zinc-100 flex items-center justify-center text-xl font-serif font-bold text-zinc-400">
            {talent.name[0]}
          </div>
          <span class="text-xs font-semibold px-2.5 py-1 rounded-full flex items-center gap-1.5 
            {talent.status === 'Available' ? 'bg-emerald-50 text-emerald-700' : 'bg-amber-50 text-amber-700'}">
            <span class="w-1.5 h-1.5 rounded-full {talent.status === 'Available' ? 'bg-emerald-500' : 'bg-amber-500'}"></span>
            {talent.status}
          </span>
        </div>
        <h3 class="font-serif text-zinc-900 text-lg font-medium">{talent.name}</h3>
        <p class="text-zinc-500 text-xs mt-0.5">{talent.role}</p>
        <p class="text-zinc-400 text-xs mt-2">{talent.exp}</p>
      </div>
      
      <div class="mt-6">
        <a href={whatsappUrl} target="_blank" class="block w-full text-center text-xs font-semibold py-2.5 rounded-lg border border-zinc-200 text-zinc-700 hover:bg-zinc-50 transition-all">
          {talent.status === 'Available' ? 'Book This Professional' : 'Join Waiting List'}
        </a>
      </div>
    </div>
  {/each}
</div>