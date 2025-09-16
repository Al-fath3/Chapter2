import Link from "next/link";
import Image from "next/image";
const PortfolioPage = () => {

  const projects = [
    {
      title: "Landing Page Website",
      desc: "Website company profile dengan desain modern.",
      img: "/project.jpeg",
    },
    {
      title: "Mobile App UI",
      desc: "UI/UX mobile application",
      img: "/project2.jpeg",
    },
    {
      title: "memorizer of the Quran",
      desc: "memorizer of the 3 juz of the Quran",
      img: "/project4.jpeg",
    },
  ];

  return (
    <div
      className="min-h-screen bg-cover bg-center relative"
      style={{ backgroundImage: `url('/bg.jpg')` }}
    >
      {/* Overlay */}
      <div className="absolute inset-0 bg-black/50"></div>

      

      {/* Content */}
      <section className="relative z-10 pt-32 pb-16 container mx-auto max-w-screen-lg px-6 text-white">
        <h2 className="text-4xl font-bold mb-12 text-center">My Portfolio</h2>
        <div className="grid md:grid-cols-3 gap-8">
          {projects.map((project, index) => (
            <div
              key={index}
              className="bg-white/10 backdrop-blur-md rounded-2xl shadow-lg overflow-hidden hover:scale-105 transition"
            >
              <img
                src={project.img}
                alt={project.title}
                className="w-full h-48 object-cover"
              />
              <div className="p-6">
                <h3 className="text-xl font-semibold mb-2">{project.title}</h3>
                <p className="text-gray-300">{project.desc}</p>
              </div>
            </div>
          ))}
        </div>
      </section>
    </div>
  );
}
export default PortfolioPage
