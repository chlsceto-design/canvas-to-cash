# canvas-to-cash
Canvas to Cash – Learn Canva. Earn Income
import React from "react";
import { SiCanva } from "react-icons/si";
import { Check } from "lucide-react";

// Single-file React component (Tailwind CSS required in your project)
// Replace logoSrc and coverSrc with your images or uploads.

const logoSrc = "/images/canvas-to-cash-logo.png"; // replace with your logo path
const coverSrc = "/images/canvas-to-cash-cover.jpg"; // replace with your cover path

export default function CanvasToCashLanding() {
  return (
    <div className="min-h-screen bg-gray-50 text-gray-900">
      {/* Header */}
      <header className="bg-white shadow-sm">
        <div className="max-w-6xl mx-auto px-6 py-4 flex items-center justify-between">
          <div className="flex items-center gap-3">
            <img src={logoSrc} alt="Canvas to Cash" className="w-12 h-12 object-contain rounded-md" />
            <div>
              <h1 className="text-lg font-bold">Canvas to Cash</h1>
              <p className="text-sm text-gray-500">Learn Canva. Earn Income.</p>
            </div>
          </div>
          <nav className="flex items-center gap-4">
            <a className="text-sm hover:underline" href="#courses">Courses</a>
            <a className="text-sm hover:underline" href="#pricing">Pricing</a>
            <a className="text-sm hover:underline" href="#testimonials">Testimonials</a>
            <a className="inline-block bg-violet-600 text-white px-4 py-2 rounded-md text-sm shadow-sm" href="#enroll">Enroll Now</a>
          </nav>
        </div>
      </header>

      {/* Hero */}
      <section className="relative">
        <div className="max-w-6xl mx-auto px-6 py-16 grid grid-cols-1 lg:grid-cols-2 gap-10 items-center">
          <div>
            <h2 className="text-4xl md:text-5xl font-extrabold leading-tight">Turn Canva skills into income</h2>
            <p className="mt-4 text-lg text-gray-600">Practical, step-by-step courses that teach you how to design fast, sell services and digital products, and grow a profitable side hustle using Canva.</p>

            <div className="mt-6 flex gap-4">
              <a href="#enroll" className="bg-violet-600 text-white px-5 py-3 rounded-md font-medium shadow">Get Started</a>
              <a href="#courses" className="px-5 py-3 rounded-md border border-gray-200 text-sm">See Courses</a>
            </div>

            <ul className="mt-8 grid grid-cols-1 sm:grid-cols-2 gap-3 text-gray-700">
              <li className="flex items-center gap-2"><Check size={16} /> Lifetime access to templates</li>
              <li className="flex items-center gap-2"><Check size={16} /> Real money-making workflows</li>
              <li className="flex items-center gap-2"><Check size={16} /> Templates, scripts & resources</li>
              <li className="flex items-center gap-2"><Check size={16} /> Community & live Q&amp;A</li>
            </ul>
          </div>

          <div className="relative">
            <div className="rounded-2xl overflow-hidden shadow-lg">
              <img src={coverSrc} alt="Canvas to Cash cover" className="w-full h-80 object-cover" />
            </div>
            <div className="absolute right-6 bottom-6 bg-white rounded-lg p-4 shadow-md w-64">
              <div className="flex items-center gap-3">
                <div className="bg-violet-100 p-2 rounded-md"><SiCanva size={28} className="text-violet-600" /></div>
                <div>
                  <div className="text-sm font-semibold">Mini-course: 5-day Canva Cash</div>
                  <div className="text-xs text-gray-500">Create sellable designs in 5 days</div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>

      {/* Courses */}
      <section id="courses" className="max-w-6xl mx-auto px-6 py-12">
        <h3 className="text-2xl font-semibold">Courses &amp; Workshops</h3>
        <p className="text-gray-600 mt-2">Short, actionable modules — perfect for beginners and hustlers.</p>

        <div className="mt-6 grid grid-cols-1 md:grid-cols-3 gap-6">
          {[
            {
              title: "Canva Basics to Profit",
              desc: "From setup to first sale — templates, listings, and pricing.",
              price: "$49"
            },
            {
              title: "Social Media Templates Kit",
              desc: "Create high-converting posts & ads fast.",
              price: "$29"
            },
            {
              title: "Client Workflow Mastery",
              desc: "Package your services, onboard clients, and scale.",
              price: "$79"
            }
          ].map((c) => (
            <article key={c.title} className="bg-white rounded-xl p-5 shadow-sm">
              <h4 className="font-semibold">{c.title}</h4>
              <p className="mt-2 text-sm text-gray-600">{c.desc}</p>
              <div className="mt-4 flex items-center justify-between">
                <div className="text-lg font-bold">{c.price}</div>
                <a href="#enroll" className="text-sm px-3 py-2 bg-violet-600 text-white rounded">Enroll</a>
              </div>
            </article>
          ))}
        </div>
      </section>

      {/* Pricing / CTA */}
      <section id="pricing" className="bg-white border-t mt-6">
        <div className="max-w-4xl mx-auto px-6 py-12 text-center">
          <h3 className="text-2xl font-semibold">Ready to start earning?</h3>
          <p className="text-gray-600 mt-2">Choose your plan and get instant access to templates, videos, and community.</p>

          <div className="mt-8 flex flex-col md:flex-row gap-6 justify-center">
            <div className="p-6 rounded-xl border w-full md:w-64">
              <div className="text-sm text-gray-500">Starter</div>
              <div className="text-3xl font-bold mt-2">$29</div>
              <p className="text-sm text-gray-600 mt-2">Access to 2 starter courses + templates</p>
              <a href="#enroll" className="mt-4 inline-block px-4 py-2 bg-violet-600 text-white rounded">Choose</a>
            </div>

            <div className="p-6 rounded-xl border-2 border-violet-600 w-full md:w-64">
              <div className="text-sm text-gray-500">Pro</div>
              <div className="text-3xl font-bold mt-2">$79</div>
              <p className="text-sm text-gray-600 mt-2">All courses, templates &amp; live Q&amp;A</p>
              <a href="#enroll" className="mt-4 inline-block px-4 py-2 bg-violet-600 text-white rounded">Choose</a>
            </div>
          </div>
        </div>
      </section>

      {/* Testimonials */}
      <section id="testimonials" className="max-w-6xl mx-auto px-6 py-12">
        <h3 className="text-2xl font-semibold">What students say</h3>
        <div className="mt-6 grid grid-cols-1 md:grid-cols-3 gap-6">
          {[1, 2, 3].map((i) => (
            <blockquote key={i} className="bg-white p-5 rounded-xl shadow-sm">
              <p className="text-gray-700">“This course helped me land my first client and replace a part-time income — totally worth it!”</p>
              <footer className="mt-3 text-sm text-gray-500">— Student {i}</footer>
            </blockquote>
          ))}
        </div>
      </section>

      {/* Enroll / Newsletter */}
      <section id="enroll" className="bg-gradient-to-r from-violet-600 to-pink-500 text-white py-12 mt-8">
        <div className="max-w-4xl mx-auto px-6 text-center">
          <h3 className="text-2xl font-bold">Join Canvas to Cash</h3>
          <p className="mt-2">Get a free starter template when you sign up.</p>

          <form className="mt-6 flex flex-col sm:flex-row gap-3 justify-center">
            <input type="email" placeholder="Your email" className="px-4 py-3 rounded-md text-gray-900 w-full sm:w-80" />
            <button className="px-6 py-3 bg-white rounded-md font-semibold">Get Access</button>
          </form>
        </div>
      </section>

      {/* Footer */}
      <footer className="bg-white border-t mt-12">
        <div className="max-w-6xl mx-auto px-6 py-8 flex flex-col md:flex-row items-center justify-between">
          <div className="flex items-center gap-3">
            <img src={logoSrc} alt="logo" className="w-10 h-10 object-contain" />
            <div>
              <div className="font-semibold">Canvas to Cash</div>
              <div className="text-sm text-gray-500">Learn Canva. Earn Income.</div>
            </div>
          </div>

          <div className="mt-4 md:mt-0 text-sm text-gray-600">© {new Date().getFullYear()} Canvas to Cash. All rights reserved.</div>
        </div>
      </footer>
    </div>
  );
}
