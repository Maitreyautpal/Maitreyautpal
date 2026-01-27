


import { motion } from "framer-motion";
import { Github, Linkedin, Mail, MapPin, Sparkles } from "lucide-react";
const HeroSection = () => {
  const badges = [{
    label: "Python",
    color: "primary"
  }, {
    label: "Data Science",
    color: "secondary"
  }, {
    label: "AI & ML",
    color: "accent"
  }, {
    label: "GitHub",
    color: "primary"
  }];
  return <section className="relative min-h-screen flex items-center justify-center overflow-hidden">
      {/* Background effects */}
      <div className="absolute inset-0 grid-pattern opacity-30" />
      <div className="absolute inset-0 bg-hero-glow" />
      
      {/* Floating orbs */}
      <motion.div className="absolute top-1/4 left-1/4 w-64 h-64 rounded-full bg-primary/5 blur-3xl" animate={{
      y: [-20, 20, -20],
      x: [-10, 10, -10]
    }} transition={{
      duration: 8,
      repeat: Infinity,
      ease: "easeInOut"
    }} />
      <motion.div className="absolute bottom-1/4 right-1/4 w-80 h-80 rounded-full bg-secondary/5 blur-3xl" animate={{
      y: [20, -20, 20],
      x: [10, -10, 10]
    }} transition={{
      duration: 10,
      repeat: Infinity,
      ease: "easeInOut"
    }} />

      <div className="container relative z-10 px-6">
        <motion.div initial={{
        opacity: 0,
        y: 30
      }} animate={{
        opacity: 1,
        y: 0
      }} transition={{
        duration: 0.8
      }} className="max-w-4xl mx-auto text-center">
          {/* Terminal-style intro */}
          <motion.div initial={{
          opacity: 0,
          scale: 0.95
        }} animate={{
          opacity: 1,
          scale: 1
        }} transition={{
          delay: 0.2
        }} className="terminal-window mb-8 inline-block">
            <div className="terminal-header">
              <span className="terminal-dot bg-red-500" />
              <span className="terminal-dot bg-yellow-500" />
              <span className="terminal-dot bg-green-500" />
              <span className="ml-4 text-sm text-muted-foreground font-mono">portfolio.tsx</span>
            </div>
            <div className="p-4 font-mono text-sm text-left">
              <span className="text-muted-foreground">const</span>{" "}
              <span className="text-secondary">developer</span>{" "}
              <span className="text-muted-foreground">=</span>{" "}
              <span className="text-primary">"Maitreya Utpal"</span>
              <span className="text-muted-foreground">;</span>
            </div>
          </motion.div>

          {/* Name */}
          <motion.h1 initial={{
          opacity: 0,
          y: 20
        }} animate={{
          opacity: 1,
          y: 0
        }} transition={{
          delay: 0.4
        }} className="text-5xl md:text-7xl font-bold mb-4">
            <span className="text-foreground">Hi, I'm </span>
            <span className="gradient-text glow-text-primary">Maitreya Utpal </span>
            <span className="inline-block ml-3">
              <Sparkles className="w-10 h-10 text-primary animate-pulse" />
            </span>
          </motion.h1>

          {/* Role */}
          <motion.div initial={{
          opacity: 0,
          y: 20
        }} animate={{
          opacity: 1,
          y: 0
        }} transition={{
          delay: 0.5
        }} className="mb-6">
            <h2 className="text-2xl md:text-3xl font-mono text-secondary glow-text-secondary">
              Aspiring Data Science | AI & ML
            </h2>
          </motion.div>

          {/* Location */}
          <motion.div initial={{
          opacity: 0
        }} animate={{
          opacity: 1
        }} transition={{
          delay: 0.6
        }} className="flex items-center justify-center gap-2 text-muted-foreground mb-6">
            <MapPin className="w-4 h-4 text-primary" />
            <span className="font-mono text-sm">India</span>
          </motion.div>

          {/* Tagline */}
          <motion.p initial={{
          opacity: 0,
          y: 20
        }} animate={{
          opacity: 1,
          y: 0
        }} transition={{
          delay: 0.7
        }} className="text-xl md:text-2xl text-muted-foreground mb-8 max-w-2xl mx-auto">
            Building intelligent systems with{" "}
            <span className="text-primary">data</span>,{" "}
            <span className="text-secondary">code</span>, and{" "}
            <span className="text-accent">curiosity</span>.
          </motion.p>

          {/* Badges */}
          <motion.div initial={{
          opacity: 0,
          y: 20
        }} animate={{
          opacity: 1,
          y: 0
        }} transition={{
          delay: 0.8
        }} className="flex flex-wrap justify-center gap-3 mb-10">
            {badges.map((badge, index) => <motion.span key={badge.label} initial={{
            opacity: 0,
            scale: 0.8
          }} animate={{
            opacity: 1,
            scale: 1
          }} transition={{
            delay: 0.9 + index * 0.1
          }} className={`tech-badge ${badge.color === "primary" ? "border-primary/30 text-primary" : badge.color === "secondary" ? "border-secondary/30 text-secondary" : "border-accent/30 text-accent"}`}>
                {badge.label}
              </motion.span>)}
          </motion.div>

          {/* Social Links */}
          <motion.div initial={{
          opacity: 0,
          y: 20
        }} animate={{
          opacity: 1,
          y: 0
        }} transition={{
          delay: 1.1
        }} className="flex justify-center gap-4">
            <a href="https://github.com/maitreyautpal" target="_blank" rel="noopener noreferrer" className="p-3 rounded-xl bg-card border border-border hover:border-primary/50 hover:bg-primary/10 transition-all duration-300 group">
              <Github className="w-6 h-6 text-muted-foreground group-hover:text-primary transition-colors" />
            </a>
            <a href="https://linkedin.com/in/maitreyautpal" target="_blank" rel="noopener noreferrer" className="p-3 rounded-xl bg-card border border-border hover:border-secondary/50 hover:bg-secondary/10 transition-all duration-300 group">
              <Linkedin className="w-6 h-6 text-muted-foreground group-hover:text-secondary transition-colors" />
            </a>
            <a href="mailto:maitreyautpal@gmail.com" className="p-3 rounded-xl bg-card border border-border hover:border-accent/50 hover:bg-accent/10 transition-all duration-300 group">
              <Mail className="w-6 h-6 text-muted-foreground group-hover:text-accent transition-colors" />
            </a>
          </motion.div>
        </motion.div>

        {/* Scroll indicator */}
        <motion.div initial={{
        opacity: 0
      }} animate={{
        opacity: 1
      }} transition={{
        delay: 1.5
      }} className="absolute bottom-10 left-1/2 -translate-x-1/2">
          <motion.div animate={{
          y: [0, 10, 0]
        }} transition={{
          duration: 2,
          repeat: Infinity
        }} className="w-6 h-10 rounded-full border-2 border-muted-foreground/30 flex items-start justify-center p-2">
            <motion.div className="w-1.5 h-1.5 rounded-full bg-primary" />
          </motion.div>
        </motion.div>
      </div>
    </section>;
};
export default HeroSection;




