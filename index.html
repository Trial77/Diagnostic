import React, { useState, useEffect, useRef } from "react";
import {
  FlaskConical, Shield, Clock, Home, Download, ChevronRight, Check,
  Plus, Minus, X, Calendar, Phone, MessageCircle, User, MapPin,
  Activity, Heart, Zap, Star, ArrowRight, Bell, FileText, Eye,
  Loader2, CheckCircle2, AlertTriangle, XCircle, ChevronDown,
  Droplets, Stethoscope, TrendingUp, Package, Lock, RefreshCw,
  Truck, TestTube, BarChart3, Info, ChevronLeft, Menu, ChevronUp
} from "lucide-react";

// ─── DESIGN TOKENS ───────────────────────────────────────────────────────────
const C = {
  navy: "#0A1628",
  blue: "#1B4FD8",
  teal: "#0D9488",
  tealLt: "#14B8A6",
  sky: "#E0F2FE",
  white: "#FFFFFF",
  slate50: "#F8FAFC",
  slate100: "#F1F5F9",
  slate200: "#E2E8F0",
  slate400: "#94A3B8",
  slate600: "#475569",
  slate700: "#334155",
  slate800: "#1E293B",
  green: "#059669",
  greenLt: "#D1FAE5",
  amber: "#D97706",
  amberLt: "#FEF3C7",
  red: "#DC2626",
  redLt: "#FEE2E2",
};

// ─── MOCK DATA ────────────────────────────────────────────────────────────────
const PACKAGES = [
  {
    id: 1, name: "Full Body Checkup", icon: Activity, price: 1299, originalPrice: 2500,
    badge: "Most Popular", badgeColor: C.blue,
    tests: ["CBC", "Blood Sugar (F)", "Lipid Profile", "Liver Function", "Kidney Function", "Thyroid (TSH)", "Urine Routine"],
    testCount: 72, turnaround: "6 hours", description: "Comprehensive wellness screening"
  },
  {
    id: 2, name: "Cardiac Health", icon: Heart, price: 999, originalPrice: 1800,
    badge: "Heart Care", badgeColor: "#BE123C",
    tests: ["Lipid Profile", "Troponin I", "CK-MB", "Homocysteine", "hsCRP", "ECG Analysis"],
    testCount: 28, turnaround: "4 hours", description: "Complete cardiovascular risk assessment"
  },
  {
    id: 3, name: "Senior Citizen Profile", icon: Shield, price: 1599, originalPrice: 3000,
    badge: "60+ Years", badgeColor: C.teal,
    tests: ["CBC", "Blood Sugar (PP)", "HbA1c", "Vitamin D", "Vitamin B12", "Bone Profile", "PSA (Men)", "CA 125 (Women)"],
    testCount: 98, turnaround: "8 hours", description: "Age-appropriate health monitoring"
  },
  {
    id: 4, name: "Diabetes Care", icon: Droplets, price: 699, originalPrice: 1200,
    badge: "Diabetes", badgeColor: "#7C3AED",
    tests: ["HbA1c", "Fasting Blood Sugar", "Post-Prandial Sugar", "Insulin Level", "Kidney Function", "Urine Microalbumin"],
    testCount: 18, turnaround: "5 hours", description: "Comprehensive diabetes management panel"
  },
  {
    id: 5, name: "Women's Wellness", icon: Stethoscope, price: 1199, originalPrice: 2200,
    badge: "Women's Health", badgeColor: "#DB2777",
    tests: ["Hormonal Panel", "Thyroid Profile", "Iron Studies", "CBC", "Vitamin D", "CA 125", "PCOD Markers"],
    testCount: 54, turnaround: "6 hours", description: "Tailored for women's health needs"
  },
  {
    id: 6, name: "Executive Health", icon: TrendingUp, price: 2499, originalPrice: 4500,
    badge: "Premium", badgeColor: "#B45309",
    tests: ["Full Body", "Stress Hormones", "Heavy Metals", "Nutritional Panel", "Genetic Markers", "Body Composition"],
    testCount: 142, turnaround: "12 hours", description: "Elite annual health intelligence report"
  }
];

const TIME_SLOTS = [
  { id: 1, time: "6:00 AM – 8:00 AM", note: "Fasting Required", popular: true },
  { id: 2, time: "8:00 AM – 10:00 AM", note: "Fasting Required", popular: true },
  { id: 3, time: "10:00 AM – 12:00 PM", note: "Post-meal acceptable" },
  { id: 4, time: "12:00 PM – 2:00 PM", note: "Post-meal acceptable" },
  { id: 5, time: "2:00 PM – 4:00 PM", note: "Post-meal acceptable" },
  { id: 6, time: "4:00 PM – 6:00 PM", note: "Evening slot" },
];

const MOCK_ORDERS = [
  {
    id: "HX-20240315-001",
    packages: ["Full Body Checkup"],
    date: "15 Mar 2024",
    status: "Report Ready",
    amount: 1299,
    phlebotomist: "Rajesh Kumar",
    reportAvailable: true,
  },
  {
    id: "HX-20240308-002",
    packages: ["Cardiac Health"],
    date: "8 Mar 2024",
    status: "Processing",
    amount: 999,
    phlebotomist: "Priya Nair",
    reportAvailable: false,
  },
  {
    id: "HX-20240301-003",
    packages: ["Diabetes Care"],
    date: "1 Mar 2024",
    status: "Sample Collected",
    amount: 699,
    phlebotomist: "Anand Sharma",
    reportAvailable: false,
  },
];

const REPORT_DATA = {
  patient: "Ramesh Gupta", age: 42, gender: "Male", date: "15 Mar 2024",
  orderId: "HX-20240315-001",
  sections: [
    {
      name: "Complete Blood Count",
      tests: [
        { name: "Hemoglobin", value: 14.2, unit: "g/dL", ref: "13.5 – 17.5", status: "optimal" },
        { name: "WBC Count", value: 7800, unit: "cells/μL", ref: "4500 – 11000", status: "optimal" },
        { name: "Platelet Count", value: 185000, unit: "/μL", ref: "150000 – 400000", status: "optimal" },
        { name: "Hematocrit", value: 42.1, unit: "%", ref: "41 – 53", status: "optimal" },
        { name: "RBC Count", value: 4.9, unit: "million/μL", ref: "4.5 – 5.9", status: "optimal" },
      ]
    },
    {
      name: "Lipid Profile",
      tests: [
        { name: "Total Cholesterol", value: 218, unit: "mg/dL", ref: "< 200", status: "borderline" },
        { name: "HDL Cholesterol", value: 38, unit: "mg/dL", ref: "> 40 (Men)", status: "borderline" },
        { name: "LDL Cholesterol", value: 148, unit: "mg/dL", ref: "< 130", status: "borderline" },
        { name: "Triglycerides", value: 195, unit: "mg/dL", ref: "< 150", status: "critical" },
        { name: "VLDL", value: 39, unit: "mg/dL", ref: "5 – 40", status: "optimal" },
      ]
    },
    {
      name: "Blood Sugar",
      tests: [
        { name: "Fasting Glucose", value: 108, unit: "mg/dL", ref: "70 – 100", status: "borderline" },
        { name: "HbA1c", value: 5.9, unit: "%", ref: "< 5.7", status: "borderline" },
      ]
    },
    {
      name: "Thyroid Function",
      tests: [
        { name: "TSH", value: 2.4, unit: "mIU/L", ref: "0.4 – 4.0", status: "optimal" },
        { name: "Free T3", value: 3.1, unit: "pg/mL", ref: "2.3 – 4.2", status: "optimal" },
        { name: "Free T4", value: 1.2, unit: "ng/dL", ref: "0.8 – 1.8", status: "optimal" },
      ]
    }
  ]
};

const STATUS_CONFIG = {
  "Phlebotomist Assigned": { color: C.blue, bg: "#EFF6FF", icon: User },
  "Sample Collected": { color: C.teal, bg: "#F0FDFA", icon: TestTube },
  "Processing": { color: C.amber, bg: "#FFFBEB", icon: Loader2 },
  "Report Ready": { color: C.green, bg: C.greenLt, icon: CheckCircle2 },
};

// ─── HELPER COMPONENTS ────────────────────────────────────────────────────────
function StatusBadge({ status }) {
  const cfg = STATUS_CONFIG[status] || {};
  const Icon = cfg.icon || Bell;
  return (
    <span style={{ background: cfg.bg, color: cfg.color, border: `1px solid ${cfg.color}22` }}
      className="inline-flex items-center gap-1.5 px-3 py-1 rounded-full text-xs font-semibold">
      <Icon size={11} className={status === "Processing" ? "animate-spin" : ""} />
      {status}
    </span>
  );
}

function ResultBadge({ status }) {
  const map = {
    optimal: { label: "Optimal", bg: C.greenLt, color: C.green },
    borderline: { label: "Borderline", bg: C.amberLt, color: C.amber },
    critical: { label: "Critical", bg: C.redLt, color: C.red },
  };
  const cfg = map[status] || map.optimal;
  return (
    <span style={{ background: cfg.bg, color: cfg.color }}
      className="inline-flex items-center px-2.5 py-0.5 rounded-full text-xs font-bold">
      {status === "optimal" && <Check size={10} className="mr-1" />}
      {status === "borderline" && <AlertTriangle size={10} className="mr-1" />}
      {status === "critical" && <XCircle size={10} className="mr-1" />}
      {cfg.label}
    </span>
  );
}

function WhatsAppToast({ message, onClose }) {
  useEffect(() => {
    const t = setTimeout(onClose, 5000);
    return () => clearTimeout(t);
  }, [onClose]);

  return (
    <div className="fixed bottom-6 right-6 z-50 animate-bounce-in">
      <div className="flex items-start gap-3 bg-white rounded-2xl shadow-2xl border border-slate-100 p-4 max-w-sm">
        <div className="w-10 h-10 rounded-full flex items-center justify-center flex-shrink-0"
          style={{ background: "#25D366" }}>
          <MessageCircle size={20} color="white" fill="white" />
        </div>
        <div className="flex-1 min-w-0">
          <div className="flex items-center justify-between mb-1">
            <span className="text-xs font-bold text-slate-500">WhatsApp • Helix Diagnostics</span>
            <button onClick={onClose} className="text-slate-400 hover:text-slate-600 ml-2">
              <X size={14} />
            </button>
          </div>
          <p className="text-sm text-slate-700 leading-relaxed whitespace-pre-line">{message}</p>
          <span className="text-xs text-slate-400 mt-1 block">just now</span>
        </div>
      </div>
    </div>
  );
}

function SuccessOverlay({ title, message, onClose }) {
  return (
    <div className="fixed inset-0 z-50 flex items-center justify-center bg-black/50 backdrop-blur-sm">
      <div className="bg-white rounded-3xl p-8 max-w-sm mx-4 text-center shadow-2xl animate-scale-in">
        <div className="w-20 h-20 rounded-full flex items-center justify-center mx-auto mb-5"
          style={{ background: C.greenLt }}>
          <CheckCircle2 size={42} style={{ color: C.green }} />
        </div>
        <h3 className="text-xl font-bold text-slate-800 mb-2">{title}</h3>
        <p className="text-slate-500 text-sm mb-6">{message}</p>
        <button onClick={onClose}
          className="w-full py-3 rounded-xl font-semibold text-white"
          style={{ background: C.blue }}>
          Continue
        </button>
      </div>
    </div>
  );
}

// ─── NAVBAR ───────────────────────────────────────────────────────────────────
function Navbar({ page, setPage, cartCount }) {
  const [scrolled, setScrolled] = useState(false);
  const [menuOpen, setMenuOpen] = useState(false);

  useEffect(() => {
    const fn = () => setScrolled(window.scrollY > 20);
    window.addEventListener("scroll", fn);
    return () => window.removeEventListener("scroll", fn);
  }, []);

  return (
    <nav className={`fixed top-0 left-0 right-0 z-40 transition-all duration-300 ${scrolled ? "shadow-lg" : ""}`}
      style={{ background: "rgba(10,22,40,0.97)", backdropFilter: "blur(12px)" }}>
      <div className="max-w-7xl mx-auto px-4 sm:px-6">
        <div className="flex items-center justify-between h-16">
          {/* Logo */}
          <button onClick={() => setPage("home")} className="flex items-center gap-2.5">
            <div className="w-8 h-8 rounded-lg flex items-center justify-center"
              style={{ background: `linear-gradient(135deg, ${C.teal}, ${C.blue})` }}>
              <FlaskConical size={18} color="white" />
            </div>
            <div className="text-left">
              <span className="text-white font-bold text-base tracking-tight leading-none block">Helix</span>
              <span className="text-xs leading-none" style={{ color: C.tealLt }}>Diagnostics</span>
            </div>
          </button>

          {/* Desktop Nav */}
          <div className="hidden md:flex items-center gap-1">
            {["home", "packages", "book", "dashboard"].map(p => (
              <button key={p} onClick={() => setPage(p)}
                className={`px-4 py-2 rounded-lg text-sm font-medium capitalize transition-colors ${page === p ? "text-white" : "text-slate-400 hover:text-white"
                  }`}
                style={page === p ? { background: "rgba(29,79,216,0.3)", color: C.tealLt } : {}}>
                {p === "book" ? "Book Test" : p === "dashboard" ? "My Reports" : p}
              </button>
            ))}
          </div>

          {/* Actions */}
          <div className="flex items-center gap-3">
            <button onClick={() => setPage("book")} className="relative hidden sm:flex items-center gap-2 px-3 py-2 rounded-lg text-sm font-semibold text-white transition-colors"
              style={{ background: "rgba(13,148,136,0.2)", border: "1px solid rgba(20,184,166,0.3)" }}>
              <Package size={15} style={{ color: C.tealLt }} />
              <span style={{ color: C.tealLt }}>Cart</span>
              {cartCount > 0 && (
                <span className="absolute -top-1.5 -right-1.5 w-5 h-5 rounded-full text-xs flex items-center justify-center text-white font-bold"
                  style={{ background: C.blue }}>
                  {cartCount}
                </span>
              )}
            </button>
            <button onClick={() => setPage("dashboard")}
              className="hidden sm:flex items-center gap-2 px-4 py-2 rounded-lg text-sm font-semibold text-white transition-all"
              style={{ background: `linear-gradient(135deg, ${C.blue}, ${C.teal})` }}>
              <Phone size={14} />
              My Reports
            </button>
            <button className="md:hidden text-white p-1.5" onClick={() => setMenuOpen(!menuOpen)}>
              <Menu size={22} />
            </button>
          </div>
        </div>

        {/* Mobile Menu */}
        {menuOpen && (
          <div className="md:hidden border-t border-white/10 py-3 pb-4 space-y-1">
            {["home", "packages", "book", "dashboard"].map(p => (
              <button key={p} onClick={() => { setPage(p); setMenuOpen(false); }}
                className="w-full text-left px-4 py-2.5 rounded-lg text-sm font-medium text-slate-300 hover:text-white hover:bg-white/10 transition-colors capitalize">
                {p === "book" ? "Book Test" : p === "dashboard" ? "My Reports" : p}
              </button>
            ))}
          </div>
        )}
      </div>
    </nav>
  );
}

// ─── HERO SECTION ─────────────────────────────────────────────────────────────
function HeroSection({ setPage }) {
  const stats = [
    { val: "6 Hrs", label: "Report Delivery" },
    { val: "50K+", label: "Tests Monthly" },
    { val: "NABL", label: "Accredited Lab" },
    { val: "99.4%", label: "Accuracy Rate" },
  ];

  return (
    <section className="relative min-h-screen flex items-center overflow-hidden"
      style={{ background: `linear-gradient(135deg, ${C.navy} 0%, #0F2A4E 50%, #0A1628 100%)` }}>
      <div className="absolute inset-0 opacity-5">
        <svg width="100%" height="100%">
          <defs>
            <pattern id="grid" width="60" height="60" patternUnits="userSpaceOnUse">
              <circle cx="30" cy="30" r="1" fill={C.teal} />
            </pattern>
          </defs>
          <rect width="100%" height="100%" fill="url(#grid)" />
        </svg>
      </div>

      <div className="absolute top-1/4 right-1/4 w-96 h-96 rounded-full opacity-10 blur-3xl pointer-events-none"
        style={{ background: C.teal }} />
      <div className="absolute bottom-1/3 left-1/4 w-64 h-64 rounded-full opacity-10 blur-3xl pointer-events-none"
        style={{ background: C.blue }} />

      <div className="relative max-w-7xl mx-auto px-4 sm:px-6 pt-24 pb-16 w-full">
        <div className="grid lg:grid-cols-2 gap-12 items-center">
          {/* Left */}
          <div>
            <div className="inline-flex items-center gap-2 px-3 py-1.5 rounded-full mb-6 text-xs font-semibold"
              style={{ background: "rgba(13,148,136,0.15)", border: "1px solid rgba(13,148,136,0.3)", color: C.tealLt }}>
              <div className="w-2 h-2 rounded-full animate-pulse" style={{ background: C.tealLt }} />
              NABL Accredited • ISO 15189 Certified
            </div>

            <h1 className="text-4xl sm:text-5xl lg:text-6xl font-black text-white leading-tight mb-4">
              Precision Diagnostics,{" "}
              <span style={{ color: C.tealLt }}>Results in 6 Hours</span>
            </h1>

            <p className="text-slate-400 text-lg leading-relaxed mb-8 max-w-lg">
              Hospital-grade blood testing from the comfort of your home. Our certified phlebotomists collect samples, and your reports are ready before your next meal.
            </p>

            <div className="flex flex-wrap gap-3 mb-12">
              <button onClick={() => setPage("packages")}
                className="flex items-center gap-2.5 px-6 py-3.5 rounded-xl font-bold text-white text-sm transition-all hover:scale-105 active:scale-95"
                style={{ background: `linear-gradient(135deg, ${C.blue}, ${C.teal})`, boxShadow: `0 4px 24px ${C.teal}44` }}>
                <Home size={16} />
                Book Home Collection
                <ArrowRight size={14} />
              </button>
              <button onClick={() => setPage("dashboard")}
                className="flex items-center gap-2.5 px-6 py-3.5 rounded-xl font-bold text-sm transition-all hover:scale-105 active:scale-95"
                style={{ background: "rgba(255,255,255,0.08)", border: "1px solid rgba(255,255,255,0.15)", color: "white" }}>
                <Download size={16} />
                Download Reports
              </button>
            </div>

            <div className="flex flex-wrap gap-4">
              {[
                { icon: Shield, text: "100% Secure Reports" },
                { icon: Clock, text: "Same-Day Collection" },
                { icon: MessageCircle, text: "WhatsApp Updates" },
              ].map(({ icon: Icon, text }) => (
                <div key={text} className="flex items-center gap-2">
                  <div className="w-7 h-7 rounded-lg flex items-center justify-center"
                    style={{ background: "rgba(13,148,136,0.15)" }}>
                    <Icon size={14} style={{ color: C.tealLt }} />
                  </div>
                  <span className="text-slate-400 text-sm">{text}</span>
                </div>
              ))}
            </div>
          </div>

          {/* Right — Stats card */}
          <div className="hidden lg:block">
            <div className="rounded-3xl p-8"
              style={{ background: "rgba(255,255,255,0.04)", border: "1px solid rgba(255,255,255,0.08)", backdropFilter: "blur(20px)" }}>
              <div className="flex items-center gap-3 mb-6">
                <div className="w-12 h-12 rounded-2xl flex items-center justify-center"
                  style={{ background: `linear-gradient(135deg, ${C.teal}, ${C.blue})` }}>
                  <FlaskConical size={22} color="white" />
                </div>
                <div>
                  <div className="text-white font-bold">Lab Intelligence Dashboard</div>
                  <div className="text-slate-500 text-xs">Live quality metrics</div>
                </div>
              </div>

              <div className="grid grid-cols-2 gap-4 mb-6">
                {stats.map(({ val, label }) => (
                  <div key={label} className="p-4 rounded-2xl"
                    style={{ background: "rgba(255,255,255,0.04)", border: "1px solid rgba(255,255,255,0.06)" }}>
                    <div className="text-2xl font-black text-white mb-1" style={{ color: C.tealLt }}>{val}</div>
                    <div className="text-slate-400 text-xs">{label}</div>
                  </div>
                ))}
              </div>

              <div className="space-y-2">
                {[
                  { test: "Hemoglobin", val: "14.2 g/dL", status: "optimal" },
                  { test: "Total Cholesterol", val: "218 mg/dL", status: "borderline" },
                  { test: "Fasting Glucose", val: "108 mg/dL", status: "borderline" },
                  { test: "TSH", val: "2.4 mIU/L", status: "optimal" },
                ].map(({ test, val, status }) => (
                  <div key={test} className="flex items-center justify-between py-2.5 px-3 rounded-xl"
                    style={{ background: "rgba(255,255,255,0.03)" }}>
                    <span className="text-slate-400 text-sm">{test}</span>
                    <div className="flex items-center gap-2">
                      <span className="text-white text-sm font-medium">{val}</span>
                      <ResultBadge status={status} />
                    </div>
                  </div>
                ))}
              </div>

              <div className="mt-4 flex items-center gap-2 text-xs text-slate-500">
                <div className="w-1.5 h-1.5 rounded-full animate-pulse" style={{ background: C.green }} />
                Sample report preview • Actual results vary
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
  );
}

// ─── PACKAGES PAGE ────────────────────────────────────────────────────────────
function PackagesPage({ cart, setCart, setPage }) {
  const [expandedId, setExpandedId] = useState(null);
  const [addedId, setAddedId] = useState(null);

  function addToCart(pkg) {
    setCart(prev => {
      const exists = prev.find(i => i.id === pkg.id);
      return exists ? prev : [...prev, { ...pkg, qty: 1 }];
    });
    setAddedId(pkg.id);
    setTimeout(() => setAddedId(null), 1800);
  }

  function inCart(id) { return cart.some(i => i.id === id); }

  return (
    <div className="min-h-screen pt-20" style={{ background: C.slate50 }}>
      <div className="py-12 px-4" style={{ background: C.navy }}>
        <div className="max-w-7xl mx-auto text-center">
          <div className="inline-flex items-center gap-2 px-3 py-1 rounded-full text-xs font-semibold mb-4"
            style={{ background: "rgba(13,148,136,0.2)", color: C.tealLt }}>
            <Package size={12} /> Health Packages
          </div>
          <h2 className="text-3xl sm:text-4xl font-black text-white mb-3">
            Choose Your Health Package
          </h2>
          <p className="text-slate-400 max-w-xl mx-auto">
            Curated panels designed by specialists. All tests performed in our NABL-accredited lab with results in 6 hours.
          </p>
        </div>
      </div>

      <div className="max-w-7xl mx-auto px-4 sm:px-6 py-10">
        <div className="grid sm:grid-cols-2 lg:grid-cols-3 gap-5">
          {PACKAGES.map(pkg => {
            const Icon = pkg.icon;
            const expanded = expandedId === pkg.id;
            const added = addedId === pkg.id;
            const isInCart = inCart(pkg.id);
            const discount = Math.round((1 - pkg.price / pkg.originalPrice) * 100);

            return (
              <div key={pkg.id}
                className="bg-white rounded-2xl overflow-hidden transition-all duration-200 hover:shadow-xl"
                style={{
                  border: isInCart ? `2px solid ${C.teal}` : "1px solid #E2E8F0",
                  boxShadow: isInCart ? `0 0 0 4px ${C.teal}15` : undefined
                }}>
                <div className="h-1.5" style={{ background: `linear-gradient(90deg, ${pkg.badgeColor}, ${C.teal})` }} />

                <div className="p-5">
                  <div className="flex items-start justify-between mb-3">
                    <div className="flex items-center gap-3">
                      <div className="w-10 h-10 rounded-xl flex items-center justify-center"
                        style={{ background: `${pkg.badgeColor}18` }}>
                        <Icon size={20} style={{ color: pkg.badgeColor }} />
                      </div>
                      <div>
                        <h3 className="font-bold text-slate-800 text-sm leading-tight">{pkg.name}</h3>
                        <span className="text-xs" style={{ color: pkg.badgeColor }}>{pkg.badge}</span>
                      </div>
                    </div>
                    <span className="text-xs px-2 py-0.5 rounded-full font-bold text-white"
                      style={{ background: C.green }}>{discount}% off</span>
                  </div>

                  <p className="text-slate-500 text-xs mb-3">{pkg.description}</p>

                  <div className="flex items-center gap-3 mb-4">
                    <div className="flex items-baseline gap-1">
                      <span className="text-2xl font-black" style={{ color: C.navy }}>₹{pkg.price.toLocaleString()}</span>
                      <span className="text-slate-400 text-sm line-through">₹{pkg.originalPrice.toLocaleString()}</span>
                    </div>
                  </div>

                  <div className="flex items-center gap-4 text-xs text-slate-500 mb-4">
                    <span className="flex items-center gap-1">
                      <TestTube size={12} style={{ color: C.teal }} />
                      {pkg.testCount} tests
                    </span>
                    <span className="flex items-center gap-1">
                      <Clock size={12} style={{ color: C.teal }} />
                      {pkg.turnaround}
                    </span>
                  </div>

                  <div className="mb-4">
                    <div className="flex flex-wrap gap-1.5">
                      {pkg.tests.slice(0, expanded ? pkg.tests.length : 3).map(t => (
                        <span key={t} className="text-xs px-2 py-0.5 rounded-md font-medium"
                          style={{ background: C.slate100, color: C.slate700 }}>{t}</span>
                      ))}
                      {!expanded && pkg.tests.length > 3 && (
                        <button onClick={() => setExpandedId(pkg.id)}
                          className="text-xs px-2 py-0.5 rounded-md font-medium transition-colors"
                          style={{ background: `${C.teal}15`, color: C.teal }}>
                          +{pkg.tests.length - 3} more
                        </button>
                      )}
                      {expanded && (
                        <button onClick={() => setExpandedId(null)}
                          className="text-xs px-2 py-0.5 rounded-md font-medium"
                          style={{ background: C.slate100, color: C.slate600 }}>
                          Show less
                        </button>
                      )}
                    </div>
                  </div>

                  <button
                    onClick={() => addToCart(pkg)}
                    disabled={isInCart}
                    className="w-full py-2.5 rounded-xl text-sm font-bold transition-all duration-200 flex items-center justify-center gap-2"
                    style={isInCart
                      ? { background: C.greenLt, color: C.green }
                      : {
                        background: added ? `${C.teal}15` : `linear-gradient(135deg, ${C.blue}, ${C.teal})`,
                        color: added ? C.teal : "white"
                      }}>
                    {isInCart ? (
                      <><Check size={15} /> Added to Cart</>
                    ) : added ? (
                      <><Check size={15} /> Added!</>
                    ) : (
                      <><Plus size={15} /> Add to Cart</>
                    )}
                  </button>
                </div>
              </div>
            );
          })}
        </div>

        {cart.length > 0 && (
          <div className="fixed bottom-6 left-1/2 -translate-x-1/2 z-30">
            <button onClick={() => setPage("book")}
              className="flex items-center gap-3 px-6 py-3.5 rounded-2xl text-white font-bold shadow-2xl transition-all hover:scale-105 active:scale-95"
              style={{
                background: `linear-gradient(135deg, ${C.blue}, ${C.teal})`,
                boxShadow: `0 8px 32px ${C.blue}55`
              }}>
              <Package size={18} />
              View Cart ({cart.length} package{cart.length !== 1 ? "s" : ""})
              <span className="px-2 py-0.5 rounded-lg text-xs font-black bg-white/20">
                ₹{cart.reduce((s, i) => s + i.price, 0).toLocaleString()}
              </span>
              <ArrowRight size={16} />
            </button>
          </div>
        )}
      </div>
    </div>
  );
}

// ─── BOOKING ENGINE ───────────────────────────────────────────────────────────
function BookingPage({ cart, setCart, setPage }) {
  const [step, setStep] = useState(1);
  const [form, setForm] = useState({ name: "", age: "", phone: "", address: "", pincode: "" });
  const [selectedDate, setSelectedDate] = useState("");
  const [selectedSlot, setSelectedSlot] = useState(null);
  const [whatsapp, setWhatsapp] = useState(true);
  const [showSuccess, setShowSuccess] = useState(false);
  const [toast, setToast] = useState(null);
  const [errors, setErrors] = useState({});

  const total = cart.reduce((s, i) => s + i.price, 0);
  const today = new Date().toISOString().split("T")[0];

  function removeFromCart(id) {
    setCart(prev => prev.filter(i => i.id !== id));
  }

  function validateStep2() {
    const e = {};
    if (!form.name.trim()) e.name = "Name is required";
    if (!form.age || form.age < 1 || form.age > 120) e.age = "Enter valid age";
    if (!form.phone.match(/^[6-9]\d{9}$/)) e.phone = "Enter valid 10-digit mobile number";
    if (!form.address.trim()) e.address = "Address is required";
    setErrors(e);
    return Object.keys(e).length === 0;
  }

  function validateStep3() {
    const e = {};
    if (!selectedDate) e.date = "Please select a date";
    if (!selectedSlot) e.slot = "Please select a time slot";
    setErrors(e);
    return Object.keys(e).length === 0;
  }

  function handleNext() {
    if (step === 1 && cart.length === 0) return;
    if (step === 2 && !validateStep2()) return;
    if (step === 3 && !validateStep3()) return;
    setErrors({});
    if (step < 4) setStep(step + 1);
  }

  function handleConfirm() {
    setShowSuccess(true);
    if (whatsapp) {
      setTimeout(() => setToast(`✅ Your booking is confirmed! Order #HX-2024-0042\n\n📍 Sample collection: ${selectedDate || "Tomorrow"}, ${TIME_SLOTS.find(s => s.id === selectedSlot)?.time || ""}\n\n🔬 Reports expected within 6 hours of sample collection.`), 1500);
    }
  }

  function handleSuccessClose() {
    setShowSuccess(false);
    setCart([]);
    setPage("dashboard");
  }

  const steps = ["Cart", "Patient Details", "Schedule", "Confirm & Pay"];

  return (
    <div className="min-h-screen pt-20" style={{ background: C.slate50 }}>
      {showSuccess && (
        <SuccessOverlay
          title="Booking Confirmed! 🎉"
          message={`Your home collection is scheduled. A certified phlebotomist will visit you at your address. Order #HX-2024-0042`}
          onClose={handleSuccessClose}
        />
      )}
      {toast && <WhatsAppToast message={toast} onClose={() => setToast(null)} />}

      <div className="max-w-3xl mx-auto px-4 sm:px-6 py-8">
        <div className="mb-8">
          <div className="flex items-center justify-between mb-3">
            {steps.map((s, i) => {
              const n = i + 1;
              const done = step > n;
              const active = step === n;
              return (
                <div key={s} className="flex items-center flex-1">
                  <div className="flex flex-col items-center">
                    <div className={`w-9 h-9 rounded-full flex items-center justify-center text-sm font-bold transition-all`}
                      style={{
                        background: done ? C.green : active ? C.blue : C.slate200,
                        color: done || active ? "white" : C.slate400
                      }}>
                      {done ? <Check size={16} /> : n}
                    </div>
                    <span className="text-xs mt-1 hidden sm:block text-center leading-tight"
                      style={{ color: active ? C.blue : done ? C.green : C.slate400 }}>
                      {s}
                    </span>
                  </div>
                  {i < steps.length - 1 && (
                    <div className="flex-1 h-0.5 mx-2 rounded"
                      style={{ background: step > n ? C.green : C.slate200 }} />
                  )}
                </div>
              );
            })}
          </div>
        </div>

        {/* Step 1: Cart */}
        {step === 1 && (
          <div>
            <h2 className="text-2xl font-black text-slate-800 mb-6">Your Cart</h2>
            {cart.length === 0 ? (
              <div className="text-center py-16 bg-white rounded-2xl border border-slate-200">
                <Package size={40} className="mx-auto mb-3 text-slate-300" />
                <p className="text-slate-500 mb-4">Your cart is empty</p>
                <button onClick={() => setPage("packages")}
                  className="px-6 py-2.5 rounded-xl text-white font-semibold text-sm"
                  style={{ background: C.blue }}>
                  Browse Packages
                </button>
              </div>
            ) : (
              <div className="space-y-3">
                {cart.map(item => {
                  const Icon = item.icon;
                  return (
                    <div key={item.id} className="bg-white rounded-2xl p-4 border border-slate-200 flex items-center gap-4">
                      <div className="w-12 h-12 rounded-xl flex items-center justify-center flex-shrink-0"
                        style={{ background: `${item.badgeColor}15` }}>
                        <Icon size={22} style={{ color: item.badgeColor }} />
                      </div>
                      <div className="flex-1 min-w-0">
                        <div className="font-bold text-slate-800">{item.name}</div>
                        <div className="text-xs text-slate-500">{item.testCount} tests • {item.turnaround} report</div>
                      </div>
                      <div className="text-right">
                        <div className="font-black text-slate-800">₹{item.price.toLocaleString()}</div>
                        <button onClick={() => removeFromCart(item.id)} className="text-xs mt-1"
                          style={{ color: C.red }}>Remove</button>
                      </div>
                    </div>
                  );
                })}

                <div className="bg-white rounded-2xl p-5 border-2 mt-4" style={{ borderColor: C.teal }}>
                  <div className="flex justify-between items-center mb-3">
                    <span className="text-slate-600">Subtotal</span>
                    <span className="font-semibold">₹{total.toLocaleString()}</span>
                  </div>
                  <div className="flex justify-between items-center mb-3">
                    <span className="text-slate-600">Home Collection Fee</span>
                    <span className="font-semibold text-green-600">FREE</span>
                  </div>
                  <div className="border-t border-slate-100 pt-3 flex justify-between items-center">
                    <span className="font-bold text-slate-800 text-lg">Total</span>
                    <span className="text-2xl font-black" style={{ color: C.navy }}>₹{total.toLocaleString()}</span>
                  </div>
                </div>

                <div className="flex items-center gap-3 p-3 rounded-xl text-sm"
                  style={{ background: `${C.teal}10`, border: `1px solid ${C.teal}25` }}>
                  <Shield size={16} style={{ color: C.teal }} />
                  <span style={{ color: C.teal }}>NABL certified results • Free home sample collection</span>
                </div>
              </div>
            )}
          </div>
        )}

        {/* Step 2: Patient Details */}
        {step === 2 && (
          <div>
            <h2 className="text-2xl font-black text-slate-800 mb-6">Patient Details</h2>
            <div className="bg-white rounded-2xl p-6 border border-slate-200 space-y-4">
              {[
                { key: "name", label: "Full Name", type: "text", icon: User, placeholder: "As per ID proof" },
                { key: "age", label: "Age", type: "number", icon: Calendar, placeholder: "Years" },
                { key: "phone", label: "Mobile Number", type: "tel", icon: Phone, placeholder: "10-digit number" },
                { key: "address", label: "Collection Address", type: "text", icon: MapPin, placeholder: "Full address for sample pickup" },
                { key: "pincode", label: "Pincode", type: "text", icon: MapPin, placeholder: "6-digit pincode" },
              ].map(({ key, label, type, icon: Icon, placeholder }) => (
                <div key={key}>
                  <label className="block text-sm font-semibold text-slate-700 mb-1.5">{label}</label>
                  <div className="relative">
                    <Icon size={16} className="absolute left-3.5 top-1/2 -translate-y-1/2"
                      style={{ color: errors[key] ? C.red : C.slate400 }} />
                    <input
                      type={type}
                      value={form[key]}
                      onChange={e => setForm(p => ({ ...p, [key]: e.target.value }))}
                      placeholder={placeholder}
                      className="w-full pl-10 pr-4 py-3 rounded-xl text-sm outline-none transition-all"
                      style={{
                        border: `1.5px solid ${errors[key] ? C.red : "#E2E8F0"}`,
                        background: errors[key] ? C.redLt : "white",
                      }}
                    />
                  </div>
                  {errors[key] && <p className="text-xs mt-1" style={{ color: C.red }}>{errors[key]}</p>}
                </div>
              ))}
            </div>
          </div>
        )}

        {/* Step 3: Schedule */}
        {step === 3 && (
          <div>
            <h2 className="text-2xl font-black text-slate-800 mb-6">Schedule Collection</h2>
            <div className="bg-white rounded-2xl p-6 border border-slate-200 mb-4">
              <label className="block text-sm font-semibold text-slate-700 mb-2">Select Date</label>
              <input
                type="date"
                min={today}
                value={selectedDate}
                onChange={e => { setSelectedDate(e.target.value); setErrors({}); }}
                className="w-full px-4 py-3 rounded-xl text-sm outline-none"
                style={{ border: `1.5px solid ${errors.date ? C.red : "#E2E8F0"}` }}
              />
              {errors.date && <p className="text-xs mt-1" style={{ color: C.red }}>{errors.date}</p>}
            </div>

            <div className="bg-white rounded-2xl p-6 border border-slate-200">
              <label className="block text-sm font-semibold text-slate-700 mb-3">Select Time Slot</label>
              <div className="grid sm:grid-cols-2 gap-3">
                {TIME_SLOTS.map(slot => (
                  <button key={slot.id}
                    onClick={() => { setSelectedSlot(slot.id); setErrors({}); }}
                    className="p-3.5 rounded-xl text-left transition-all"
                    style={{
                      border: `2px solid ${selectedSlot === slot.id ? C.teal : "#E2E8F0"}`,
                      background: selectedSlot === slot.id ? `${C.teal}10` : "white",
                    }}>
                    <div className="flex items-center justify-between mb-0.5">
                      <span className="font-bold text-sm" style={{ color: selectedSlot === slot.id ? C.teal : C.navy }}>
                        {slot.time}
                      </span>
                      {slot.popular && (
                        <span className="text-xs px-1.5 py-0.5 rounded font-semibold"
                          style={{ background: `${C.amber}20`, color: C.amber }}>Popular</span>
                      )}
                    </div>
                    <span className="text-xs" style={{ color: C.slate400 }}>{slot.note}</span>
                  </button>
                ))}
              </div>
              {errors.slot && <p className="text-xs mt-2" style={{ color: C.red }}>{errors.slot}</p>}
            </div>
          </div>
        )}

        {/* Step 4: Confirm */}
        {step === 4 && (
          <div>
            <h2 className="text-2xl font-black text-slate-800 mb-6">Review & Confirm</h2>

            <div className="bg-white rounded-2xl border border-slate-200 overflow-hidden mb-4">
              <div className="px-5 py-4 border-b border-slate-100">
                <h3 className="font-bold text-slate-700 text-sm">Packages</h3>
              </div>
              {cart.map(item => (
                <div key={item.id} className="px-5 py-3 flex justify-between border-b border-slate-50 last:border-0">
                  <span className="text-slate-700 text-sm">{item.name}</span>
                  <span className="font-semibold text-sm">₹{item.price.toLocaleString()}</span>
                </div>
              ))}
              <div className="px-5 py-3 flex justify-between bg-slate-50">
                <span className="font-bold text-slate-800">Total</span>
                <span className="font-black text-lg" style={{ color: C.navy }}>₹{total.toLocaleString()}</span>
              </div>
            </div>

            <div className="grid sm:grid-cols-2 gap-4 mb-4">
              {[
                { label: "Patient", value: form.name || "—", icon: User },
                { label: "Age", value: form.age ? `${form.age} years` : "—", icon: Calendar },
                { label: "Mobile", value: form.phone || "—", icon: Phone },
                { label: "Address", value: form.address || "—", icon: MapPin },
                { label: "Date", value: selectedDate || "—", icon: Calendar },
                { label: "Slot", value: TIME_SLOTS.find(s => s.id === selectedSlot)?.time || "—", icon: Clock },
              ].map(({ label, value, icon: Icon }) => (
                <div key={label} className="bg-white rounded-xl p-4 border border-slate-200 flex items-start gap-3">
                  <Icon size={16} className="mt-0.5 flex-shrink-0" style={{ color: C.teal }} />
                  <div>
                    <div className="text-xs text-slate-500 mb-0.5">{label}</div>
                    <div className="font-semibold text-slate-800 text-sm">{value}</div>
                  </div>
                </div>
              ))}
            </div>

            <div className="bg-white rounded-2xl border border-slate-200 p-5 mb-4">
              <div className="flex items-center justify-between">
                <div className="flex items-center gap-3">
                  <div className="w-10 h-10 rounded-xl flex items-center justify-center"
                    style={{ background: "#25D36620" }}>
                    <MessageCircle size={20} style={{ color: "#25D366" }} />
                  </div>
                  <div>
                    <div className="font-bold text-slate-800 text-sm">WhatsApp Live Tracking</div>
                    <div className="text-xs text-slate-500">Get real-time updates and report PDFs on WhatsApp</div>
                  </div>
                </div>
                <button onClick={() => setWhatsapp(p => !p)}
                  className="w-12 h-6 rounded-full transition-colors relative"
                  style={{ background: whatsapp ? "#25D366" : C.slate200 }}>
                  <span className="absolute top-0.5 transition-all w-5 h-5 bg-white rounded-full shadow"
                    style={{ left: whatsapp ? "calc(100% - 22px)" : "2px" }} />
                </button>
              </div>
              {whatsapp && (
                <div className="mt-3 p-3 rounded-xl text-xs"
                  style={{ background: "#25D36610", border: "1px solid #25D36625" }}>
                  <div className="font-semibold text-slate-700 mb-1">You'll receive notifications for:</div>
                  <ul className="space-y-0.5 text-slate-500">
                    {["Phlebotomist assignment with contact details",
                      "Sample collection confirmation",
                      "Report ready with secure PDF link"].map(t => (
                        <li key={t} className="flex items-center gap-1.5">
                          <Check size={10} style={{ color: "#25D366" }} />{t}
                        </li>
                      ))}
                  </ul>
                </div>
              )}
            </div>

            <div className="p-4 rounded-xl text-sm"
              style={{ background: `${C.blue}08`, border: `1px solid ${C.blue}20` }}>
              <div className="flex items-center gap-2 font-semibold text-slate-700 mb-1">
                <Lock size={14} style={{ color: C.blue }} /> Secure Payment
              </div>
              <p className="text-slate-500 text-xs">Pay at doorstep via cash, UPI, or card after sample collection. 100% secure.</p>
            </div>
          </div>
        )}

        {/* Navigation */}
        <div className="flex items-center gap-3 mt-6">
          {step > 1 && (
            <button onClick={() => setStep(step - 1)}
              className="flex items-center gap-2 px-5 py-3 rounded-xl text-sm font-semibold text-slate-700 border border-slate-200 bg-white">
              <ChevronLeft size={16} /> Back
            </button>
          )}
          <button
            onClick={step === 4 ? handleConfirm : handleNext}
            disabled={step === 1 && cart.length === 0}
            className="flex-1 flex items-center justify-center gap-2 py-3 rounded-xl text-sm font-bold text-white transition-all disabled:opacity-50"
            style={{ background: `linear-gradient(135deg, ${C.blue}, ${C.teal})` }}>
            {step === 4 ? (
              <><CheckCircle2 size={16} /> Confirm Booking — ₹{total.toLocaleString()}</>
            ) : step === 1 && cart.length === 0 ? (
              "Add packages to continue"
            ) : (
              <>Continue <ChevronRight size={16} /></>
            )}
          </button>
        </div>
      </div>
    </div>
  );
}

// ─── DASHBOARD / REPORTS PAGE ─────────────────────────────────────────────────
function DashboardPage() {
  const [authStep, setAuthStep] = useState("phone"); // phone | otp | dashboard
  const [phone, setPhone] = useState("");
  const [otp, setOtp] = useState(["", "", "", ""]);
  const [phoneError, setPhoneError] = useState("");
  const [otpError, setOtpError] = useState("");
  const [loading, setLoading] = useState(false);
  const [selectedOrder, setSelectedOrder] = useState(null);
  const [reportTab, setReportTab] = useState(0);
  const [toast, setToast] = useState(null);
  const otpRefs = [useRef(), useRef(), useRef(), useRef()];

  function sendOTP() {
    if (!phone.match(/^[6-9]\d{9}$/)) {
      setPhoneError("Enter a valid 10-digit mobile number");
      return;
    }
    setPhoneError("");
    setLoading(true);
    setTimeout(() => { setLoading(false); setAuthStep("otp"); }, 1200);
  }

  function handleOtpChange(i, val) {
    if (!/^\d?$/.test(val)) return;
    const next = [...otp];
    next[i] = val;
    setOtp(next);
    if (val && i < 3) otpRefs[i + 1].current?.focus();
  }

  function verifyOTP() {
    const code = otp.join("");
    if (code.length < 4) { setOtpError("Enter the 4-digit OTP"); return; }
    setLoading(true);
    setOtpError("");
    setTimeout(() => { setLoading(false); setAuthStep("dashboard"); }, 1500);
  }

  function handleDownload(orderId) {
    setToast(`📄 Report for Order ${orderId} is being prepared...\n\nYour PDF will be sent to your WhatsApp number shortly.`);
  }

  if (authStep !== "dashboard") {
    return (
      <div className="min-h-screen pt-20 flex items-center justify-center px-4"
        style={{ background: C.slate50 }}>
        {toast && <WhatsAppToast message={toast} onClose={() => setToast(null)} />}
        <div className="w-full max-w-sm">
          <div className="bg-white rounded-3xl p-8 shadow-xl border border-slate-100">
            <div className="text-center mb-7">
              <div className="w-14 h-14 rounded-2xl flex items-center justify-center mx-auto mb-4"
                style={{ background: `linear-gradient(135deg, ${C.navy}, ${C.blue})` }}>
                <Lock size={24} color="white" />
              </div>
              <h2 className="text-xl font-black text-slate-800 mb-1">
                {authStep === "phone" ? "Access Your Reports" : "Enter OTP"}
              </h2>
              <p className="text-slate-500 text-sm">
                {authStep === "phone"
                  ? "Enter your registered mobile number"
                  : `OTP sent to +91 ${phone.slice(0, 5)}xxxxx`}
              </p>
            </div>

            {authStep === "phone" ? (
              <div>
                <div className="relative mb-4">
                  <Phone size={16} className="absolute left-3.5 top-1/2 -translate-y-1/2 text-slate-400" />
                  <div className="absolute left-9 top-1/2 -translate-y-1/2 text-slate-400 text-sm font-medium border-r border-slate-200 pr-2.5">+91</div>
                  <input
                    type="tel" value={phone} onChange={e => setPhone(e.target.value.replace(/\D/g, "").slice(0, 10))}
                    placeholder="Mobile number"
                    className="w-full pl-20 pr-4 py-3 rounded-xl text-sm outline-none"
                    style={{ border: `1.5px solid ${phoneError ? C.red : "#E2E8F0"}` }}
                    onKeyDown={e => e.key === "Enter" && sendOTP()}
                  />
                </div>
                {phoneError && <p className="text-xs mb-3" style={{ color: C.red }}>{phoneError}</p>}
                <button onClick={sendOTP} disabled={loading}
                  className="w-full py-3 rounded-xl text-white font-bold text-sm flex items-center justify-center gap-2"
                  style={{ background: `linear-gradient(135deg, ${C.blue}, ${C.teal})` }}>
                  {loading ? <Loader2 size={16} className="animate-spin" /> : <Phone size={16} />}
                  {loading ? "Sending OTP..." : "Send OTP"}
                </button>
                <p className="text-center text-xs text-slate-400 mt-4">
                  Demo: use any 10-digit number starting with 6–9
                </p>
              </div>
            ) : (
              <div>
                <div className="flex gap-3 justify-center mb-4">
                  {otp.map((d, i) => (
                    <input key={i} ref={otpRefs[i]}
                      type="text" inputMode="numeric" maxLength={1} value={d}
                      onChange={e => handleOtpChange(i, e.target.value)}
                      onKeyDown={e => { if (e.key === "Backspace" && !d && i > 0) otpRefs[i - 1].current?.focus(); }}
                      className="w-14 h-14 text-center text-xl font-black rounded-xl outline-none transition-all"
                      style={{
                        border: `2px solid ${otpError ? C.red : d ? C.teal : "#E2E8F0"}`,
                        color: C.navy
                      }}
                    />
                  ))}
                </div>
                {otpError && <p className="text-xs text-center mb-3" style={{ color: C.red }}>{otpError}</p>}
                <button onClick={verifyOTP} disabled={loading}
                  className="w-full py-3 rounded-xl text-white font-bold text-sm flex items-center justify-center gap-2"
                  style={{ background: `linear-gradient(135deg, ${C.blue}, ${C.teal})` }}>
                  {loading ? <Loader2 size={16} className="animate-spin" /> : <CheckCircle2 size={16} />}
                  {loading ? "Verifying..." : "Verify & Access Reports"}
                </button>
                <button onClick={() => setAuthStep("phone")} className="w-full text-center text-xs mt-3"
                  style={{ color: C.blue }}>
                  Change number
                </button>
                <p className="text-center text-xs text-slate-400 mt-2">Demo: any 4 digits work</p>
              </div>
            )}
          </div>
        </div>
      </div>
    );
  }

  // Report Viewer Mode
  if (selectedOrder) {
    const sections = REPORT_DATA.sections;
    const currentSection = sections[reportTab];
    return (
      <div className="min-h-screen pt-20" style={{ background: C.slate50 }}>
        {toast && <WhatsAppToast message={toast} onClose={() => setToast(null)} />}
        <div className="max-w-4xl mx-auto px-4 sm:px-6 py-8">
          <div className="flex items-center gap-3 mb-6">
            <button onClick={() => setSelectedOrder(null)}
              className="p-2 rounded-lg bg-white border border-slate-200 hover:bg-slate-50 transition-colors">
              <ChevronLeft size={18} style={{ color: C.navy }} />
            </button>
            <div>
              <h2 className="text-lg font-black text-slate-800">Health Report</h2>
              <p className="text-xs text-slate-500">Order {selectedOrder.id}</p>
            </div>
          </div>

          <div className="bg-white rounded-2xl p-5 border border-slate-200 mb-5">
            <div className="flex flex-wrap items-center justify-between gap-4">
              <div className="flex items-center gap-4">
                <div className="w-12 h-12 rounded-full flex items-center justify-center text-lg font-black text-white"
                  style={{ background: `linear-gradient(135deg, ${C.blue}, ${C.teal})` }}>
                  {REPORT_DATA.patient[0]}
                </div>
                <div>
                  <div className="font-bold text-slate-800">{REPORT_DATA.patient}</div>
                  <div className="text-xs text-slate-500">Age {REPORT_DATA.age} • {REPORT_DATA.gender} • {REPORT_DATA.date}</div>
                </div>
              </div>
              <div className="flex gap-2">
                <button onClick={() => handleDownload(selectedOrder.id)}
                  className="flex items-center gap-2 px-4 py-2 rounded-xl text-sm font-semibold text-white"
                  style={{ background: `linear-gradient(135deg, ${C.blue}, ${C.teal})` }}>
                  <Download size={14} /> Download PDF
                </button>
              </div>
            </div>
          </div>

          <div className="grid grid-cols-3 gap-3 mb-5">
            {[
              { label: "Optimal", count: sections.flatMap(s => s.tests).filter(t => t.status === "optimal").length, color: C.green, bg: C.greenLt },
              { label: "Borderline", count: sections.flatMap(s => s.tests).filter(t => t.status === "borderline").length, color: C.amber, bg: C.amberLt },
              { label: "Critical", count: sections.flatMap(s => s.tests).filter(t => t.status === "critical").length, color: C.red, bg: C.redLt },
            ].map(({ label, count, color, bg }) => (
              <div key={label} className="rounded-xl p-3 text-center" style={{ background: bg }}>
                <div className="text-2xl font-black" style={{ color }}>{count}</div>
                <div className="text-xs font-semibold mt-0.5" style={{ color }}>{label}</div>
              </div>
            ))}
          </div>

          <div className="flex gap-2 overflow-x-auto pb-1 mb-4">
            {sections.map((s, i) => (
              <button key={s.name} onClick={() => setReportTab(i)}
                className="px-4 py-2 rounded-xl text-sm font-semibold whitespace-nowrap transition-all"
                style={{
                  background: reportTab === i ? C.navy : "white",
                  color: reportTab === i ? "white" : C.slate600,
                  border: `1px solid ${reportTab === i ? C.navy : "#E2E8F0"}`
                }}>
                {s.name}
              </button>
            ))}
          </div>

          <div className="bg-white rounded-2xl border border-slate-200 overflow-hidden">
            <div className="px-5 py-4 border-b border-slate-100 flex items-center gap-2">
              <BarChart3 size={16} style={{ color: C.blue }} />
              <h3 className="font-bold text-slate-800 text-sm">{currentSection.name}</h3>
            </div>
            <div className="divide-y divide-slate-50">
              {currentSection.tests.map(test => (
                <div key={test.name} className="px-5 py-4 flex items-center gap-4">
                  <div className="flex-1 min-w-0">
                    <div className="font-semibold text-slate-800 text-sm">{test.name}</div>
                    <div className="text-xs text-slate-400 mt-0.5">Reference: {test.ref}</div>
                  </div>
                  <div className="text-right">
                    <div className="font-black text-slate-800">
                      {test.value}
                      <span className="font-normal text-slate-400 text-xs ml-1">{test.unit}</span>
                    </div>
                  </div>
                  <div className="w-24 flex justify-end">
                    <ResultBadge status={test.status} />
                  </div>
                  <div className="w-16 hidden sm:block">
                    <div className="h-1.5 rounded-full bg-slate-100 overflow-hidden">
                      <div className="h-full rounded-full"
                        style={{
                          width: test.status === "optimal" ? "55%" : test.status === "borderline" ? "75%" : "95%",
                          background: test.status === "optimal" ? C.green : test.status === "borderline" ? C.amber : C.red
                        }} />
                    </div>
                  </div>
                </div>
              ))}
            </div>
          </div>

          <div className="mt-4 flex items-center gap-2 p-3 rounded-xl text-xs text-slate-500"
            style={{ background: `${C.blue}08`, border: `1px solid ${C.blue}15` }}>
            <Info size={12} style={{ color: C.blue }} />
            Report verified by Dr. Priya Sharma, MD Pathology. For medical advice, consult your physician.
          </div>
        </div>
      </div>
    );
  }

  // Standard Dashboard Layout (Orders list)
  return (
    <div className="min-h-screen pt-20" style={{ background: C.slate50 }}>
      {toast && <WhatsAppToast message={toast} onClose={() => setToast(null)} />}
      <div className="max-w-3xl mx-auto px-4 sm:px-6 py-8">
        <div className="bg-white rounded-2xl p-5 border border-slate-200 mb-6">
          <div className="flex items-center justify-between">
            <div className="flex items-center gap-4">
              <div className="w-12 h-12 rounded-full flex items-center justify-center text-lg font-black text-white"
                style={{ background: `linear-gradient(135deg, ${C.navy}, ${C.blue})` }}>R</div>
              <div>
                <div className="font-bold text-slate-800">Ramesh Gupta</div>
                <div className="text-xs text-slate-500">+91 98765 43210</div>
              </div>
            </div>
            <button onClick={() => setAuthStep("phone")} className="text-xs text-slate-400 hover:text-slate-600">
              Sign out
            </button>
          </div>
        </div>

        <h2 className="text-xl font-black text-slate-800 mb-4">Recent Orders</h2>

        <div className="space-y-4">
          {MOCK_ORDERS.map(order => (
            <div key={order.id} className="bg-white rounded-2xl border border-slate-200 overflow-hidden">
              <div className="p-5">
                <div className="flex items-start justify-between mb-3">
                  <div>
                    <div className="text-xs text-slate-400 mb-0.5 font-mono">{order.id}</div>
                    <div className="font-bold text-slate-800">{order.packages.join(", ")}</div>
                    <div className="text-xs text-slate-500 mt-0.5">{order.date}</div>
                  </div>
                  <StatusBadge status={order.status} />
                </div>

                <div className="mb-4">
                  <div className="flex items-center gap-1 mb-1.5">
                    {["Phlebotomist Assigned", "Sample Collected", "Processing", "Report Ready"].map((s, i) => {
                      const statuses = ["Phlebotomist Assigned", "Sample Collected", "Processing", "Report Ready"];
                      const curIdx = statuses.indexOf(order.status);
                      const done = i <= curIdx;
                      return (
                        <div key={s} className="flex items-center flex-1">
                          <div className="w-4 h-4 rounded-full flex items-center justify-center flex-shrink-0"
                            style={{ background: done ? C.teal : C.slate200 }}>
                            {done && <Check size={9} color="white" />}
                          </div>
                          {i < 3 && <div className="flex-1 h-0.5" style={{ background: done && i < curIdx ? C.teal : C.slate200 }} />}
                        </div>
                      );
                    })}
                  </div>
                  <div className="flex justify-between">
                    {["Assigned", "Collected", "Processing", "Ready"].map(l => (
                      <span key={l} className="text-xs text-slate-400" style={{ width: "25%", textAlign: l === "Ready" ? "right" : l === "Assigned" ? "left" : "center" }}>{l}</span>
                    ))}
                  </div>
                </div>

                <div className="flex items-center justify-between">
                  <div className="flex items-center gap-1.5 text-xs text-slate-500">
                    <User size={12} />
                    {order.phlebotomist}
                  </div>
                  <div className="font-bold" style={{ color: C.navy }}>₹{order.amount.toLocaleString()}</div>
                </div>
              </div>

              {order.reportAvailable && (
                <div className="border-t border-slate-100 px-5 py-3 flex gap-3"
                  style={{ background: C.greenLt }}>
                  <button onClick={() => setSelectedOrder(order)}
                    className="flex-1 flex items-center justify-center gap-2 py-2 rounded-xl text-sm font-semibold text-white"
                    style={{ background: C.green }}>
                    <Eye size={14} /> View Report
                  </button>
                  <button onClick={() => handleDownload(order.id)}
                    className="flex items-center gap-2 px-4 py-2 rounded-xl text-sm font-semibold"
                    style={{ background: "white", color: C.green, border: `1px solid ${C.green}` }}>
                    <Download size={14} /> PDF
                  </button>
                </div>
              )}
            </div>
          ))}
        </div>
      </div>
    </div>
  );
}

// ─── FOOTER ───────────────────────────────────────────────────────────────────
function Footer({ setPage }) {
  return (
    <footer style={{ background: C.navy }} className="py-12 px-4 mt-auto">
      <div className="max-w-7xl mx-auto">
        <div className="grid sm:grid-cols-3 gap-8 pb-8 border-b border-white/10">
          <div>
            <div className="flex items-center gap-2.5 mb-4">
              <div className="w-8 h-8 rounded-lg flex items-center justify-center"
                style={{ background: `linear-gradient(135deg, ${C.teal}, ${C.blue})` }}>
                <FlaskConical size={16} color="white" />
              </div>
              <span className="text-white font-bold">Helix Diagnostics</span>
            </div>
            <p className="text-slate-400 text-sm">NABL accredited • ISO 15189 • 200+ tests</p>
          </div>
          <div>
            <div className="text-white font-semibold mb-3 text-sm">Quick Links</div>
            {["home", "packages", "book", "dashboard"].map(p => (
              <button key={p} onClick={() => setPage(p)} className="block text-slate-400 hover:text-white text-sm mb-1.5 capitalize transition-colors text-left">
                {p === "book" ? "Book Test" : p === "dashboard" ? "My Reports" : p}
              </button>
            ))}
          </div>
          <div>
            <div className="text-white font-semibold mb-3 text-sm">Contact</div>
            <div className="space-y-2 text-slate-400 text-sm">
              <div>📞 1800-HELIX-01 (Toll Free)</div>
              <div>✉️ care@helixdiag.in</div>
              <div>🕐 7 AM – 9 PM, Mon–Sun</div>
            </div>
          </div>
        </div>
        <div className="pt-6 text-center text-slate-500 text-xs">
          © 2026 Helix Diagnostics Pvt. Ltd. All rights reserved. NABL Reg. No. MC-3801
        </div>
      </div>
    </footer>
  );
}

// ─── APP ROOT ─────────────────────────────────────────────────────────────────
export default function App() {
  const [page, setPage] = useState("home");
  const [cart, setCart] = useState([]);

  useEffect(() => { window.scrollTo({ top: 0, behavior: "smooth" }); }, [page]);

  return (
    <div className="flex flex-col min-h-screen" style={{ fontFamily: "'Inter', system-ui, sans-serif" }}>
      <style>{`
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800;900&display=swap');
        * { box-sizing: border-box; }
        input[type=number]::-webkit-outer-spin-button,
        input[type=number]::-webkit-inner-spin-button { -webkit-appearance: none; margin: 0; }
        @keyframes bounce-in { 0%{transform:scale(0.8) translateY(20px);opacity:0} 80%{transform:scale(1.02) translateY(-2px)} 100%{transform:scale(1) translateY(0);opacity:1} }
        @keyframes scale-in { 0%{transform:scale(0.85);opacity:0} 100%{transform:scale(1);opacity:1} }
        .animate-bounce-in { animation: bounce-in 0.4s cubic-bezier(.23,1.2,.32,1) forwards; }
        .animate-scale-in { animation: scale-in 0.3s cubic-bezier(.23,1.2,.32,1) forwards; }
      `}</style>

      <Navbar page={page} setPage={setPage} cartCount={cart.length} />

      <main className="flex-1">
        {page === "home" && <HeroSection setPage={setPage} />}
        {page === "packages" && <PackagesPage cart={cart} setCart={setCart} setPage={setPage} />}
        {page === "book" && <BookingPage cart={cart} setCart={setCart} setPage={setPage} />}
        {page === "dashboard" && <DashboardPage />}
      </main>

      {page !== "home" && <Footer setPage={setPage} />}
    </div>
  );
}