import React, { useState } from "react";

export default function App() {
  const [posts, setPosts] = useState([]);
  const [newPost, setNewPost] = useState("");
  const [newMedia, setNewMedia] = useState(null);
  const [chatMessages, setChatMessages] = useState([]);
  const [newMessage, setNewMessage] = useState("");

  const [executives] = useState([
    {
      name: "Festus Musa Jabati",
      role: "President",
      details: {
        address: "L60 Looking Town, Wilberforce Barracks",
        contact: "+23278122557",
        email: "festusmusa18@gmail.com",
      },
    },
    {
      name: "Hassan Bellay",
      role: "Vice President",
      details: {
        address: "Wilberforce",
        dob: "14 December 1993",
        pob: "Kenema District, Eastern Province",
        contact: "+23288443828",
      },
    },
    {
      name: "Alusine Bellay",
      role: "Chairman",
      details: {
        address: "Wilberforce",
        dob: "14 December 1993",
        pob: "Kenema District, Eastern Province",
      },
    },
    { name: "[Executive Vice Chairman’s Name]", role: "Executive Vice Chairman" },
    { name: "[Chairlady’s Name]", role: "Chairlady" },
    { name: "[Financial Secretary’s Name]", role: "Financial Secretary" },
    {
      name: "Alhaji Mamoud Sheriff",
      role: "Public Relations Officer (PRO)",
      details: {
        address: "Imatt",
        contact: "+23280202919 / +23274267725",
        pob: "Kenema District, Eastern Province",
        dob: "14 March 1997",
        email: "sheriffalhajim409@gmail.com",
      },
    },
    { name: "[Deputy PRO’s Name]", role: "Deputy PRO" },
    { name: "Kadija F Kabia", role: "Discipline Officer" },
    { name: "[Organizing Secretary’s Name]", role: "Organizing Secretary" },
    { name: "[Secretary’s Name]", role: "Secretary" },
  ]);

  const handleAddPost = () => {
    if (newPost.trim() !== "" || newMedia) {
      setPosts([
        {
          text: newPost,
          media: newMedia,
          date: new Date().toLocaleString(),
          comments: [],
        },
        ...posts,
      ]);
      setNewPost("");
      setNewMedia(null);
    }
  };

  const handleAddComment = (index, comment) => {
    if (comment.trim() === "") return;
    const updatedPosts = [...posts];
    updatedPosts[index].comments.push({ text: comment, date: new Date().toLocaleString() });
    setPosts(updatedPosts);
  };

  const handleSendMessage = () => {
    if (newMessage.trim() === "") return;
    setChatMessages([...chatMessages, { text: newMessage, date: new Date().toLocaleString() }]);
    setNewMessage("");
  };

  return (
    <div
      className="min-h-screen text-gray-900"
      style={{
        backgroundImage: "url('/family-background.jpg')",
        backgroundSize: "cover",
        backgroundPosition: "center",
      }}
    >
      <div className="min-h-screen bg-black bg-opacity-50">
        {/* Header */}
        <header className="bg-gradient-to-r from-black via-gray-800 to-black text-white p-6 flex justify-between items-center shadow-lg">
          <h1 className="text-2xl font-bold tracking-wide">UNITED FAMILY</h1>
          <nav>
            <ul className="flex space-x-6">
              <li><a href="#about" className="hover:text-red-400 transition">About</a></li>
              <li><a href="#executives" className="hover:text-red-400 transition">Executives</a></li>
              <li><a href="#posts" className="hover:text-red-400 transition">Posts</a></li>
              <li><a href="#chat" className="hover:text-red-400 transition">Chat</a></li>
              <li><a href="#donate" className="hover:text-red-400 transition">Donate</a></li>
              <li><a href="#contact" className="hover:text-red-400 transition">Contact</a></li>
            </ul>
          </nav>
        </header>

        {/* Hero Section */}
        <section className="relative text-center py-24 text-white shadow-xl">
          <div className="relative z-10">
            <img src="/logo.png" alt="United Family Logo" className="mx-auto w-40 mb-6 drop-shadow-2xl" />
            <h2 className="text-5xl font-extrabold mb-4 drop-shadow-md">Welcome to United Family</h2>
            <p className="text-lg max-w-2xl mx-auto drop-shadow-sm">
              A community built on love, unity, and togetherness. We stand as one,
              support each other, and grow stronger every day.
            </p>
            <p className="mt-4 text-xl font-semibold drop-shadow-lg">Together We Stand</p>
          </div>
        </section>

        {/* About Section */}
        <section id="about" className="py-16 px-6 md:px-20 bg-white bg-opacity-90 rounded-xl shadow-md mt-10">
          <h3 className="text-3xl font-semibold text-center mb-8 text-red-600">About Us</h3>
          <p className="max-w-3xl mx-auto text-lg text-center text-gray-800">
            United Family is more than just an organization – it is a beacon of hope, love, and unity. We are a family bound not by blood, but by purpose, compassion, and the drive to see each other succeed. Our mission is to uplift, inspire, and empower every individual, creating a space where no one is left behind. We believe that when hearts come together, mountains can be moved, dreams can be achieved, and communities can be transformed. United Family is a symbol of resilience, discipline, and togetherness – where every voice matters, every effort counts, and every dream is nurtured. We are not just building a community; we are shaping a legacy of love and strength for generations to come.
          </p>
        </section>

        {/* Executives Section */}
        <section id="executives" className="py-16 px-6 md:px-20 bg-gradient-to-br from-red-50 via-white to-red-100 rounded-xl shadow-inner mt-10">
          <h3 className="text-3xl font-semibold text-center mb-8 text-red-600">Our Executives</h3>
          <div className="max-w-4xl mx-auto grid md:grid-cols-2 gap-8">
            {executives.map((exec, index) => (
              <div key={index} className="p-6 bg-white shadow-xl rounded-2xl text-center">
                <h4 className="text-xl font-bold text-gray-900">{exec.name}</h4>
                <p className="text-gray-600">{exec.role}</p>
                {exec.details && (
                  <div className="mt-3 text-sm text-gray-700 space-y-1">
                    {exec.details.address && <p><strong>Address:</strong> {exec.details.address}</p>}
                    {exec.details.contact && <p><strong>Contact:</strong> {exec.details.contact}</p>}
                    {exec.details.email && <p><strong>Email:</strong> {exec.details.email}</p>}
                    {exec.details.dob && <p><strong>Date of Birth:</strong> {exec.details.dob}</p>}
                    {exec.details.pob && <p><strong>Place of Birth:</strong> {exec.details.pob}</p>}
                  </div>
                )}
              </div>
            ))}
          </div>
        </section>

        {/* Posts Section */}
        <section id="posts" className="py-16 px-6 md:px-20 bg-white bg-opacity-95 rounded-xl shadow-md mt-10">
          <h3 className="text-3xl font-semibold text-center mb-8 text-red-600">Community Posts</h3>
          <div className="max-w-2xl mx-auto">
            <textarea value={newPost} onChange={(e) => setNewPost(e.target.value)} placeholder="Write something..." className="w-full p-4 border rounded-lg" />
            <input type="file" accept="image/*,video/*" onChange={(e) => setNewMedia(URL.createObjectURL(e.target.files[0]))} className="mt-2" />
            <button onClick={handleAddPost} className="mt-4 bg-red-600 text-white px-6 py-2 rounded-lg">Post</button>
            <div className="mt-8 space-y-4">
              {posts.map((post, index) => (
                <div key={index} className="p-4 bg-gray-50 rounded-lg shadow">
                  {post.media && (post.media.endsWith(".mp4") ? (
                    <video controls className="mb-2 w-full rounded"><source src={post.media} type="video/mp4" /></video>
                  ) : (
                    <img src={post.media} alt="Post media" className="mb-2 w-full rounded" />
                  ))}
                  <p className="text-gray-800">{post.text}</p>
                  <p className="text-xs text-gray-500 mt-2">{post.date}</p>
                  <div className="mt-2">
                    {post.comments.map((c, i) => (
                      <div key={i} className="bg-white border p-2 rounded mt-1">
                        <p className="text-gray-800 text-sm">{c.text}</p>
                        <p className="text-xs text-gray-500">{c.date}</p>
                      </div>
                    ))}
                    <input type="text" placeholder="Write a comment..." onKeyDown={(e) => { if (e.key === "Enter") { handleAddComment(index, e.target.value); e.target.value = ""; } }} className="mt-2 w-full border rounded p-2 text-sm" />
                  </div>
                </div>
              ))}
            </div>
          </div>
        </section>

        {/* Chat Section */}
        <section id="chat" className="py-16 px-6 md:px-20 bg-white bg-opacity-95 rounded-xl shadow-md mt-10">
          <h3 className="text-3xl font-semibold text-center mb-8 text-red-600">Live Chat</h3>
          <div className="max-w-2xl mx-auto p-4 bg-gray-50 rounded-lg shadow">
            <div className="h-64 overflow-y-auto border p-2 mb-4 bg-white rounded">
              {chatMessages.length === 0 && <p className="text-gray-500 text-center">No messages yet. Start the conversation!</p>}
              {chatMessages.map((msg, i) => (
                <div key={i} className="mb-2">
                  <p className="text-gray-800 text-sm">{msg.text}</p>
                  <p className="text-xs text-gray-500">{msg.date}</p>
                </div>
              ))}
            </div>
            <div className="flex space-x-2">
              <input type="text" value={newMessage} onChange={(e) => setNewMessage(e.target.value)} placeholder="Type your message..." className="flex-grow border rounded p-2 text-sm" />
              <button onClick={handleSendMessage} className="bg-red-600 text-white px-4 py-2 rounded">Send</button>
            </div>
          </div>
        </section>

        {/* Donation Section */}
        <section id="donate" className="py-16 px-6 md:px-20 bg-gradient-to-r from-red-100 via-white to-red-50 rounded-xl shadow-md mt-10 text-center">
          <h3 className="text-3xl font-semibold text-red-600 mb-6">Support Our Mission</h3>
          <p className="max-w-2xl mx-auto text-lg text-gray-700 mb-6">Your generous contributions help us continue to build unity and support our community.</p>
          <a href="https://www.paypal.com/donate" target="_blank" rel="noopener noreferrer" className="inline-block bg-red-600 text-white px-8 py-3 rounded-full shadow-lg hover:bg-red-700 transition">Make a Donation</a>
        </section>

        {/* Contact Section */}
        <section id="contact" className="py-16 px-6 md:px-20 bg-white bg-opacity-90 rounded-xl shadow-md mt-10">
          <h3 className="text-3xl font-semibold text-center mb-8 text-red-600">Contact Us</h3>
          <ul className="text-center space-y-2 mb-6">
            <li><a href="tel:+23280202919" className="text-red-600 hover:underline">+232 80 202919</a></li>
            <li><a href="tel:+23278122557" className="text-red-600 hover:underline">+232 78 122557</a></li>
            <li><a href="tel:+23233574489" className="text-red-600 hover:underline">+232 33 574489</a></li>
          </ul>
          <div className="text-center space-x-4">
            <a href="https://wa.me/23280202919" target="_blank" rel="noopener noreferrer" className="inline-block bg-green-500 text-white px-6 py-3 rounded-full shadow-lg hover:bg-green-600 transition">Chat on WhatsApp</a>
            <a href="https://facebook.com/UnitedFamily" target="_blank" rel="noopener noreferrer" className="inline-block bg-blue-600 text-white px-6 py-3 rounded-full shadow-lg hover:bg-blue-700 transition">Visit Facebook Page</a>
          </div>
        </section>

        {/* Footer */}
        <footer className="bg-gradient-to-r from-black via-gray-800 to-black text-white text-center py-6 mt-10">
          <p>© {new Date().getFullYear()} United Family. All Rights Reserved.</p>
        </footer>
      </div>
    </div>
  );
}
