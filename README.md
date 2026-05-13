export default function PhoenixStore() { const products = { Steam: [ { name: 'Steam Bronze Random Key', price: '4 AZN', desc: '3$-29$' }, { name: 'Steam Gold Random Key', price: '6 AZN', desc: '8$-75$' }, { name: 'Steam Diamond Key', price: '8 AZN', desc: '15$-200$' }, ], PSN: [ { name: 'PSN Wallet 10$', price: '5 AZN' }, { name: 'PSN Wallet 20$', price: '10 AZN' }, { name: 'PSN Wallet 30$', price: '15 AZN' }, ], GooglePlay: [ { name: 'Google Play 5$', price: '2 AZN' }, { name: 'Google Play 10$', price: '5 AZN' }, { name: 'Google Play 15$', price: '8 AZN' }, ], };

return ( <div className="min-h-screen bg-black text-white"> <header className="flex items-center justify-between p-4 border-b border-zinc-800 bg-zinc-950"> <div className="text-2xl font-bold text-cyan-400">☰ PHOENIXSTORE.AZ</div>

<div className="flex gap-4 items-center">
      <input
        placeholder="Search..."
        className="bg-zinc-900 border border-zinc-700 rounded-xl px-3 py-2"
      />

      <div className="flex gap-2 text-sm">
        <button className="bg-zinc-800 px-3 py-1 rounded-lg">🇦🇿 Azərbaycan</button>
        <button className="bg-zinc-800 px-3 py-1 rounded-lg">🇹🇷 Türkçe</button>
        <button className="bg-zinc-800 px-3 py-1 rounded-lg">🇬🇧 English</button>
      </div>

      <button className="bg-cyan-500 text-black px-4 py-2 rounded-xl font-bold">
        Login / Register
      </button>
    </div>
  </header>

  <div className="flex">
    <aside className="w-64 bg-zinc-950 border-r border-zinc-800 p-4 min-h-screen">
      <h2 className="text-xl font-bold mb-4">Games</h2>

      <div className="space-y-3">
        <button className="w-full bg-zinc-900 p-3 rounded-xl text-left hover:bg-cyan-500 hover:text-black">
          Steam Key
        </button>
        <button className="w-full bg-zinc-900 p-3 rounded-xl text-left hover:bg-cyan-500 hover:text-black">
          PSN Wallet
        </button>
        <button className="w-full bg-zinc-900 p-3 rounded-xl text-left hover:bg-cyan-500 hover:text-black">
          Free Fire Diamond
        </button>
        <button className="w-full bg-zinc-900 p-3 rounded-xl text-left hover:bg-cyan-500 hover:text-black">
          PUBG UC
        </button>
        <button className="w-full bg-zinc-900 p-3 rounded-xl text-left hover:bg-cyan-500 hover:text-black">
          Robux
        </button>
        <button className="w-full bg-zinc-900 p-3 rounded-xl text-left hover:bg-cyan-500 hover:text-black">
          Google Play Gift Card
        </button>
      </div>
    </aside>

    <main className="flex-1 p-6">
      <div className="bg-red-700 rounded-2xl p-6 text-center text-3xl font-bold mb-8 shadow-lg">
        STOK QURTARIB
      </div>

      <h1 className="text-3xl font-bold mb-6 text-cyan-400">Popular Products</h1>

      <div className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
        {Object.values(products)
          .flat()
          .map((item, index) => (
            <div
              key={index}
              className="bg-zinc-900 border border-zinc-800 rounded-2xl p-5 hover:border-cyan-400 transition"
            >
              <div className="text-5xl mb-4">🎮</div>
              <h2 className="text-xl font-bold">{item.name}</h2>
              {item.desc && (
                <p className="text-zinc-400 mt-2">{item.desc}</p>
              )}
              <div className="mt-4 text-2xl font-bold text-cyan-400">
                {item.price}
              </div>

              <button className="w-full mt-5 bg-cyan-500 text-black py-3 rounded-xl font-bold hover:scale-105 transition">
                Buy Now
              </button>
            </div>
          ))}
      </div>
    </main>
  </div>
</div>

); }
