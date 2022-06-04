<script>
	import Svelvet from "svelvet";

	const initialNodes = [
	  {
	    id: 1,
	    position: { x: 217, y: 34 },
	    data: { label: "Setup Game" },
	    width: 175,
	    height: 40,
	    bgColor: "white"
	  },
	  {
	    id: 2,
	    position: { x: 216, y: 119 },
	    data: { label: "Pre-roll" },
	    width: 175,
	    height: 40,
	    bgColor: "white"
	  },
	  {
	    id: 3,
	    position: { x: 291, y: 208 },
	    data: { label: "Roll Idle" },
	    width: 175,
	    height: 40,
	    bgColor: "white"
	  },
	  {
	    id: 4,
	    position: { x: 385, y: 302 },
	    data: { label: "Resolve Dice" },
	    width: 175,
	    height: 40,
	    bgColor: "white"
	  },
    {
	    id: 5,
	    position: { x: 188, y: 377 },
	    data: { label: "Leave Tokyo?" },
	    width: 175,
	    height: 40,
	    bgColor: "white"
	  },
    {
      id: 6,
	    position: { x: 138, y: 547 },
      data: { label: "Buy Cards" },
      width: 175,
      height: 40,
      bgColor: "white"
    },
    {
	    id: 7,
	    position: { x: 38, y: 284 },
	    data: { label: "Turn Ended" },
	    width: 175,
	    height: 40,
	    bgColor: "white"
	  },
    {
	    id: 8,
	    position: { x: 408, y: 444 },
	    data: { label: "Game Ended" },
	    width: 175,
	    height: 40,
	    bgColor: "white"
	  }
	];
  
	const initialEdges = [
	  { id: "e1-2", source: 1, target: 2, label: "Done" },
	  { id: "e2-3", source: 2, target: 3, label: "Done" },
	  { id: "e3-4", source: 3, target: 4, label: "By Choice or 2x re-rolls" },
	  { id: "e4-6", source: 4, target: 6, label: "Resolved all Dice" },
	  { id: "e4-5", source: 4, target: 5, label: "Tokyo attacked" },
	  { id: "e5-6", source: 5, target: 6, label: "CP enters Tokyo" },
	  { id: "e6-7", source: 6, target: 7, label: "Done" },
	  { id: "e7-2", source: 7, target: 2, label: "Done" },
	  { id: "e4-8", source: 4, target: 8, label: "Last Monster Standing" },
	  { id: "e6-8", source: 6, target: 8, label: "20 Victory Points" },
	];
</script>

<Svelvet nodes={initialNodes} edges={initialEdges} background />
